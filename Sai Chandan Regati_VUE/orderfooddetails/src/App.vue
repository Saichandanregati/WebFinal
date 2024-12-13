<template>
  <div >
    <Myname  :customerName="Name" />

    <FoodOrdersDetails  :data="foodOrders" />

    <Myfooter :quote="delicious" />

    <div v-if="loading">Data Loading....</div>
    <div v-if="error">{{ errortofetchdata }}</div>
  </div>
</template>

<script>
import Myname from './components/Myname.vue';
import FoodOrdersDetails  from './components/FoodOrdersDetails.vue';
import Myfooter from './components/Myfooter.vue';


export default {
  name: 'App',
  components: {
    Myname,
    FoodOrdersDetails,
    Myfooter,
  },
  data() {
    return {
    
      Name: 'Sai Chandan Regati',
      foodOrders: [],
      delicious: 'Have a delicious food.',
      loading: true,
      error: null,
    };
  },
  methods: {
    async fetchorders() {
      try {
        const response = await fetch('https://saichandanregati-webnodefinal-2.onrender.com/api');
        if (!response.ok) {
          throw new Error('Network response not ok');
        }

        const data = await response.json();
        this.foodOrders =data;
      } catch (error) {
        console.error('Error fetching details of the order:', error.message);
        this.error = 'Error.Please try again later.';
        return [];
      } finally {
        this.loading = false;
      }
    },
  },
  async created() {
    await this.fetchorders();

    
  },
};
</script>

<style>
body {
  font-family: 'Montserrat', sans-serif;
  margin: 0;
  padding: 0;
}

#app div {
  margin-top: 10px;
  font-weight: bold;
  color: black;
}



</style>

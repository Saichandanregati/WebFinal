
<template>
    <div class="orders">
    <div v-for="orderitem in data" :key="orderitem.id" class="order_item">
    <h3> Restaurant Name: {{ orderitem.Restaurant_Name }} <hr></h3>
    <p>Menu: {{ orderitem.Menu }} </p>
    <p>Number of Orders: {{ orderitem.Orders }} </p>
    <p>Billing: {{ orderitem.Billing }} </p>
    <p>Payment Method: {{ orderitem.TypeOfPayment }} </p>
    <p>Total Items: {{ orderitem.NumberOfItems }} </p>
    <p> Rating: {{ orderitem.Rating }} </p>
    <p> Food Review: {{ orderitem.Reviews }} </p>
    </div>
  </div>
    </template>
    
    <script>
    export default {
        
        name: 'OrdersDetails' ,
    props: {
    data: Array,
    },
    };
    </script>
    
    <style>
    .orders {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));

      grid-gap: 30px;

      background-color: #fc6311;
      padding: 20px 20px 35px 20px;
    }
    .orders h3{
         text-align: center;

         color: rgb(0, 0, 0)
    }


    .orders p{
      color:rgb(0, 0, 0);
    }
    
    .order_item {
      background-color:rgb(255, 158, 89);
      padding-bottom: 10px;
      padding: 20px;
      
    }
    </style>
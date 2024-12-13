<!-- eslint-disable vue/multi-word-component-names -->
// eslint-disable-next-line vue/multi-word-component-names
<template>
        <ul>
         
  <li> <b><i>User Name: {{ customerName }}</i></b></li>
</ul>

  </template>
  
  <script>
  export default {
    props: {
      customerName: {
        type: String,
        required: true,
      },
    },
  };
  </script>
  
  <style >
  
  ul {
  list-style-type: none;
  padding: 0;
  margin: 0;
  overflow: hidden;
  background-color: #ff0000;;
  display: flex;
  align-items: center;
}

li {
    flex:1;
}

li{
  display: block;
  color: rgb(18, 17, 17);
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}




  </style>
  
  

<template>
  <div class="ui secondary menu">
    <div class="ui container">
      <div class="left menu">
        <router-link class="item" to="/">
          <img
            class="ui small image"
            src="../assets/logo.png"
            alt="Ecommerce"
          />
        </router-link>
        <template v-for="category in categories" :key="category.id">
          <router-link class="item" :to="category.slug">
            {{category.title}}
          </router-link>
        </template>        
      </div>
      <div class="right menu">
        <router-link class="item" to="/login" v-if="!token"> Iniciar Sesion </router-link> |
        <router-link class="item" to="/contacto"> Contáctanos </router-link>
      
      <template v-if="token">
        <router-link class="item" to="/orders">Pedidos</router-link>
        <span class="ui item cart"><i class="shopping cart icon"></i></span>
        <span class="ui item logout" @click="logout"><i class="sign-out icon"></i></span>
      </template>
      
      </div>
    </div>
  </div>
</template>

<script>
import {ref, onMounted} from 'vue';
import { getTokenApi, deleteTokenApi } from '../api/token.js'
import {getCategoriesApi} from  '../api/category';

export default {
  name: "menu",

  setup(){

    let categories=ref(null);

    onMounted(async() =>{
      const response=await getCategoriesApi();
      categories.value=response;
    });

    const token=getTokenApi();
    
    const logout= () =>{
      console.log("Cerrar sesión");    
      deleteTokenApi();
      location.replace('/')
    };


    return{
      token,
      logout,
      categories,
    }
  }
};
</script>

<style lang="scss" scoped>
.ui.menu.secondary {
  background-color: #316b83;
  .item {
    color: #ffffff;
    &:hover {
      color: #d5bfbf;
    }
  }
  .menu.left {
    width: 50%;
    .ui.image {
      width: 50px;
    }
  }
  .menu.right {
    width: 50%;
    justify-content: flex-end;
    .logout,
    .cart {
      &:hover {
        cursor: pointer;
      }
    }
  }
}
</style>

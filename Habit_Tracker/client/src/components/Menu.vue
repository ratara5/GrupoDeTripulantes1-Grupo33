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
      </div>
      <div class="right menu">
        <router-link class="item" to="/login"> Iniciar Sesion </router-link> |
        <router-link class="item" to="/contacto"> Contáctanos </router-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "menu",
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

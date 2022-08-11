<script setup>
import Logo from "./icons/Logo.vue";

</script>

<template>
  <div class="logo">
    <Logo/>
  </div>
</template>

<style>

.logo {
  display: flex;
  margin-top: 40px;
  justify-content: center;
}

@media (min-width:480px) {
  .logo {
      margin-top: 48px;
      margin-left: 39px;
      justify-content: left;
  }
}

@media (min-width: 769px) {
  .logo {
    margin-top: 81px;
    margin-left: 165px;
  }
}
</style>
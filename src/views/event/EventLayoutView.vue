<template>
  <div v-if="GStore.auctionItem">
    <h1>{{ GStore.auctionItem.description }}</h1>
    <div id="nav">
      <router-link :to="{ name: 'EventDetails' }">Details</router-link>
      |
      <router-link :to="{ name: 'EventRegister' }">Register</router-link>
      |
      <router-link :to="{ name: 'EventEdit' }">Edit</router-link>
    </div>
    <router-view :auctionItem="GStore.auctionItem" />
  </div>
</template>
<script>
export default {
  inject: ['GStore']
}
</script>

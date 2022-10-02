<template>
  <div v-if="auctionItem">
    <h1>{{ auctionItem.description }}</h1>
    <p>{{ auctionItem.time }} on {{ auctionItem.date }}</p>
  </div>
</template>

<script>
import EventService from '@/services/AuctionService.js'

export default {
  props: ['id'],
  data() {
    return {
      auctionItem: null
    }
  },
  created() {
    // fetch event (by id) and set local event data
    EventService.getAuctionItem(this.id)
      .then((response) => {
        this.auctionItem = response.data
      })
      .catch((error) => {
        console.log(error)
      })
  }
}
</script>

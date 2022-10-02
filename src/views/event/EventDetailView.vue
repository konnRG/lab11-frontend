<template>
  <p>{{ auctionItem.time }} on {{ auctionItem.date }}</p>
</template>

<script>
export default {
  props: ['id', 'auctionItem']
}
</script>

<template>
  <div v-for="listing in listings " :key="listing.id">
    <Link :href="`/listing/${listing.id}`" >
      <Listingaddress :listing="listing" />
     </Link>
  </div>

</template>
<script setup>
  import {Link} from '@inertiajs/inertia-vue3';
  import Listingaddress from '../../Components/ListingAddress.vue'
   defineProps({
    listings: Array,
  })
</script>
<script>
 import MainLayout from '../../Layouts/MainLayout.vue'
export default {
  layout: MainLayout
}
</script>

<template>
  <Link href="/listing">Listings</Link>&nbsp;
 <Link href="/listing/create">New Listing</Link>
  <div v-if="flashSuccess" class="success">
    {{ flashSuccess }}
  </div>


  <!-- <div>The page with time {{timer}}</div> -->
  <slot>Default</slot>
</template>
<script setup>
  import {computed} from 'vue';
  import {Link, usePage } from'@inertiajs/inertia-vue3';
 // import {ref} from 'vue';

  //page.props.value.flash.success
 const page = usePage()
 const flashSuccess = computed(
  ()=>page.props.value.flash.success,
  )
  // const timer = ref(0);
  // setInterval(() => timer.value++, 1000)
</script>

<style scoped>
  .success {
    background-color: green;
    color: white;

  }
</style>

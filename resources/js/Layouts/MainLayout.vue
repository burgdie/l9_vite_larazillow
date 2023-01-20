<template>
  <Link href="/">Main Page</Link>&nbsp;
  <Link href="/hello">Show Page</Link>&nbsp;
<Link href="/listing/create">Create</Link>
  <div v-if="flashSuccess" class="success">
    {{ flashSuccess }}
  </div>
  <!-- <div>
    {{ y }}
  </div> -->

  <!-- <div>The page with time {{timer}}</div> -->
  <slot>Default</slot>
</template>
<script setup>
  import {computed} from 'vue';
  import {Link, usePage } from'@inertiajs/inertia-vue3';
 // import {ref} from 'vue';

  // const x = ref(0);
  // const y = computed(() => x.value * 2)

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

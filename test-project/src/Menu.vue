
<template>
  <ul>
    <li v-for="(item, index) in myList" :key="index">{{ item }}</li>
  </ul>
</template>

<script>
    export default {
        props: ["myList"],
    }
</script>
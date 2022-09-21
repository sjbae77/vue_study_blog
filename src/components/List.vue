<template>
  <ul class="list-group list-group-flush" style="padding:50px">
    <li class="list-group-item" v-for="(a, i) in blog" :key="i" style="padding:20px">
      <h5 @click="$router.push(`/detail/${i}`)">{{ blog[i].title }}</h5>
      <p>{{ blog[i].content }}</p>
      <p>{{ blog[i].date }}</p>
      <p>{{ blog[i].number }}</p>
    </li>
  </ul>
  
</template>

<script>
export default {
    name: "List",
    props: {
        blog: Array
    }
}
</script>

<style>

</style>
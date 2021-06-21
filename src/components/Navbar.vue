<template>
  <nav>
      <ul>
        <li v-for="list,index in item"
      :key="index" >{{list.name}}</li>

      </ul>
  </nav>
</template>

<script>
export default {
    name: "Navbar", 
    props: ["item"]
}
</script>

<style lang="scss" scoped>

ul {
    margin: 0;
    padding: 0; 

    li {
        display: inline-block;
        list-style: none;
        text-transform: uppercase;
        cursor: pointer;
        margin: 15px 40px 15px 0;
        font-weight: bold;
        color: #444444;

        &:hover {
            color: #0088cc;
        }

        &:active {
            color: #0088cc;
        }

    }
}
</style>
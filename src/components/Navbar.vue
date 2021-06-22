<template>
  <nav>
        <ul>
            <li v-for="list,index in item"
        :key="index" >{{list.name}}</li>

        </ul>

        <div class="searchbar">
            <input type="text">
            <i class="fas fa-search"></i>
        </div>
  </nav>
</template>

<script>
export default {
    name: "Navbar", 
    props: ["item"]
}
</script>

<style lang="scss" scoped>

nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    
    .searchbar {

        display: flex;
        align-items: center;

        input {
            height: 20px;
            margin: 10px;
        }
    }

}

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
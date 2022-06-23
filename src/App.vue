<template>
<titles></titles>
  <div class="container">
    <Menu></Menu>
    <item_list></item_list>
  </div>
</template>

<script>
import Menu from '@/components/menu'
import item_list from '@/components/item_list'
import titles from '@/components/titles'
export default {
  name: 'App',
  components: {
    Menu,
    item_list,
    titles
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Source+Sans+Pro:wght@400;600&display=swap');

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Source Sans Pro', sans-serif;
}

.container {
  display: flex;
  flex-direction: row;
}

#app {
  margin: 32px;
  background: rgba(255, 254, 251, 0.8);

}
</style>

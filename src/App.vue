<template>
  <titles></titles>
  <div class="container">
    <Menu @add-product="addItem"></Menu>
    <item_list v-bind:product="product" @remove-item="removeItem"></item_list>
  </div>
</template>

<script>
import Menu from '@/components/menu'
import item_list from '@/components/item_list'
import titles from '@/components/titles'
export default {
  name: 'App',
  data() {
    return {
      product: [
        {
          id: 1, name: 'Наименование товара', img_link: 'https://static1.makeuseofimages.com/wordpress/wp-content/uploads/2022/01/white-polaroid-onestep-2-instant-camera-featured-image-cropped.jpg', about: 'Довольно-таки интересное описание товара в несколько строк.', price: '10000'
        },
        {
          id: 2, name: 'Консоль PlayStation 5', img_link: 'https://www.ixbt.com/img/n1/news/2020/10/3/5f9b00f9e1a5b094_1920xH_large.png', about: 'Консоль PS5 открывает новые игровые возможности, о которых вы даже не могли мечтать.', price: '49990'
        },
        {
          id: 3, name: 'Электрокарт Ninebot GoKart Pro', img_link: 'https://avatars.mds.yandex.net/get-mpic/5235397/img_id7133506827535742414.jpeg/orig', about: 'Lва титана в сфере технологий Segway и Ninebot представили новинку, которая сочетает в себе само балансирующий сегвей и полномерный картинг.', price: '149990'
        },
        {
          id: 4, name: 'Автомобиль Daewoo Matiz', img_link: 'https://otoparcalog.com/wp-content/uploads/Daewoo-Matiz.jpeg', about: 'Малолитражный городской автомобиль. Разработан и выпускается южнокорейским подразделением Daewoo.', price: '239000'
        }
      ]
    }
  },
  methods: {
    removeItem(id) {
      this.product = this.product.filter(t => t.id !== id)
    },
    addItem(item) {
      this.product.push(item)
    }
  },
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

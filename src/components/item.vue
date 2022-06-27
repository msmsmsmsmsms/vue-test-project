<template>
    <div class="item">
        <div class="rm" v-on:click="$emit('remove-item', p.id)"><img src="@/assets/rm.png"></div>
        <div class="photo">
            <img v-bind:src="p.img_link" alt="Фото_товара">
        </div>
        <h2>{{ p.name }}</h2>
        <p>{{ p.about }}</p>
        <h1>{{ p.price + ' руб.' }}</h1>
    </div>
</template>

<script> 

export default {
    props: {
        p: {
            type: Object,
            required: true
        }
    }
}
</script>

<style scoped>
.rm {
    position: absolute;
    right: -8px;
    top:-8px;
    background: #FF8484;
    width: 32px;
    height: 32px;
    box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.1);
    border-radius: 10px;
    padding: 6px;
    display: none;
}

.item:hover .rm {
    display: initial;
}

.item {
    position: relative;
    width: 332px;
    height: 423px;
    box-shadow: 0px 20px 30px rgba(0, 0, 0, 0.04), 0px 6px 10px rgba(0, 0, 0, 0.02);
    border-radius: 4px;
    margin-left: 16px;
    margin-bottom: 16px;
    color: #3f3f3f;
}

.photo {
    width: 332px;
    height: 200px;
    margin-bottom: 16px;
    border-radius: 4px;
}

img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: 4px;
}

h2 {
    padding: 0 16px;
    font-weight: 600;
    font-size: 20px;
    color: #3F3F3F;
    margin-bottom: 16px;
}

p {
    height: 80px;
    padding: 0 16px;
    font-weight: 400;
    font-size: 16px;
    color: #3F3F3F;
    margin-bottom: 32px;
}

h1 {
    padding: 0 16px;
    font-weight: 600;
    font-size: 24px;
}
</style>
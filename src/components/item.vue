<template>
    <div class="item">
        <div class="photo">
            <img src="https://static1.makeuseofimages.com/wordpress/wp-content/uploads/2022/01/white-polaroid-onestep-2-instant-camera-featured-image-cropped.jpg"
                alt="Фото_товара">
        </div>
        <h2>Наименование товара</h2>
        <p>Довольно-таки интересное описание товара в несколько строк. Довольно-таки интересное описание товара в
            несколько строк</p>
        <h1>10 000 руб.</h1>
    </div>
</template>

<script>

</script>

<style scoped>
.item {
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
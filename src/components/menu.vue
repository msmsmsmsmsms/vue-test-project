<template>
    <div class="menu">
        <form>
            <h2>Наимеенование товара</h2>
            <input type="text" name="name" id="name" placeholder="Введите наименование товара" autocomplete="off"
                required>
            <h2>Описание товара</h2>
            <textarea name="text" id="about" cols="30" rows="10" placeholder="Введите описание товара"
                autocomplete="off"></textarea>
            <h2>Ссылка на изображение товара</h2>
            <input type="url" name="url" id="url" placeholder="Введите ссылку" autocomplete="off" required>
            <h2>Цена товара</h2>
            <input type="number" name="price" id="price" placeholder="Введите цену" autocomplete="off" required>
            <button type="submit" id="submit">Добавить товар</button>
        </form>
    </div>

</template>

<script>
</script>

<style scoped>
.menu {
    flex-shrink: 0;
}

form {
    position: sticky;
    top: 24px;
    display: flex;
    width: 332px;
    flex-direction: column;
    height: 440px;
    background: #FFFEFB;
    box-shadow: 0px 20px 30px rgba(0, 0, 0, 0.04), 0px 6px 10px rgba(0, 0, 0, 0.02);
    border-radius: 4px;
    padding: 24px;
}

h1 {
    font-size: 28px;
    font-weight: 600;
    color: #3F3F3F;
    margin-bottom: 16px;
}

h2 {
    margin: 0;
    font-size: 10px;
    margin-bottom: 4px;
    font-weight: 400;
    color: #49485E;
}

input,
textarea {
    border: 0;
    height: 36px;
    background: #FFFEFB;
    box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
    border-radius: 4px;
    padding: 10px 16px;
    margin-bottom: 16px;
    font-size: 12px;
    color: #3F3F3F;
}

#about {
    height: 108px;
    resize: none;
}

#submit {
    border: 0;
    font-size: 12px;
    font-weight: 600;
    padding: 10px;
    background: #EEEEEE;
    border-radius: 10px;
    color: #B4B4B4;
}

input[type="number"]::-webkit-outer-spin-button,
input[type="number"]::-webkit-inner-spin-button {
    -webkit-appearance: none;
}

input[type='number'],
input[type="number"]:hover,
input[type="number"]:focus {
    appearance: none;
    -moz-appearance: textfield;
}

::-webkit-input-placeholder {
    color: #B4B4B4;
}

::-moz-placeholder {
    color: #B4B4B4;
}

/* Firefox 19+ */
:-moz-placeholder {
    color: #B4B4B4;
}

/* Firefox 18- */
:-ms-input-placeholder {
    color: #B4B4B4;
}
</style>
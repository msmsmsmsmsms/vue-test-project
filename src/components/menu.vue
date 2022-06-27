<template>
    <div class="menu">
        <form @submit.prevent="onSubmit" v-on:change="isFilled" @input="onInput">
            <h2>Наимеенование товара<sup> &#8226;</sup></h2>
            <input type="text" id="name" placeholder="Введите наименование товара" autocomplete="off" v-model="name"
                required>
            <small id='error_name'>Поле является обязательным</small>
            <h2>Описание товара</h2>
            <textarea id="about" cols="30" rows="10" placeholder="Введите описание товара" autocomplete="off"
                v-model="about"></textarea>
            <h2>Ссылка на изображение товара<sup> &#8226;</sup></h2>
            <input type="url" id="url" placeholder="Введите ссылку" autocomplete="off" required v-model="img_src">
            <small id='error_url'>Поле является обязательным</small>
            <h2>Цена товара<sup> &#8226;</sup></h2>
            <input type="number" id="price" placeholder="Введите цену" autocomplete="off" required v-model="price">
            <small id='error_price'>Поле является обязательным</small>
            <button type="submit" class="not_active" id="submit">Добавить товар</button>
        </form>
    </div>

</template>

<script>

export default {
    data() {
        return {
            name: '',
            about: '',
            price: '',
            img_src: ''
        }
    },
    methods: {
        onSubmit() {
            console.log(this.name)
            if (this.name.trim()) {
                var temp = this.price
                var temp_price = '' + temp
                if (temp_price.trim()) {
                    if (this.img_src.trim()) {
                        const new_p = {
                            id: Date.now(),
                            name: this.name,
                            price: temp_price,
                            img_link: this.img_src,
                            about: this.about
                        }
                        this.$emit('add-product', new_p)
                        this.name = ''
                        this.price = ''
                        this.img_src = ''
                        this.about = ''
                    }
                }
            }
            const btn = document.getElementById('submit')
            btn.classList.replace('active', 'not_active')
        },
        isFilled() {
            if (this.name.trim()) {
                if (this.price != 0) {
                    if (this.img_src.trim()) {
                        const btn = document.getElementById('submit')
                        btn.classList.replace('not_active', 'active')
                    }
                }
            }
        },
        onInput() {
            if (this.name.trim()) {
                document.getElementById('error_name').style.opacity = '0'
            }
            else {
                document.getElementById('error_name').style.opacity = '1'
            }
            if (this.price != 0) {
                document.getElementById('error_price').style.opacity = '0'
            }
            else {
                document.getElementById('error_price').style.opacity = '1'
            }
            if (this.img_src.trim()) {
                document.getElementById('error_url').style.opacity = '0'
            }
            else {
                document.getElementById('error_url').style.opacity = '1'
            }
        }
    }
}

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

small {
    height: 10px;
    color: #FF8484;
    font-size: 8px;
    font-weight: 400px;
    margin-bottom: 2px;

}

input,
textarea {
    border: 0;
    height: 36px;
    background: #FFFEFB;
    box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
    border-radius: 4px;
    padding: 10px 16px;
    margin-bottom: 4px;
    font-size: 12px;
    color: #3F3F3F;
    outline: none;
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
    border-radius: 10px;
    margin-top: 20px;
}

#submit.not_active {
    cursor: default;
    background: #EEEEEE;
    color: #B4B4B4;
}

#submit.active {
    cursor: pointer;
    background: #7BAE73;
    color: #fff;
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

input:invalid:focus {
    border: 1px solid #FF8484;
}

input:valid:focus {
    border: 1px solid #7BAE73;
}

sup {
    color: #FF8484;
}
</style>
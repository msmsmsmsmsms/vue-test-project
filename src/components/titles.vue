<template>
    <div class="titles">
        <h1>Добавление товара</h1>
        <filter_btn></filter_btn>
    </div>
</template>

<script>
import filter_btn from '@/components/filter_btn'
export default {
    name: 'titles',
    components: {
        filter_btn
    }
}
</script>

<style scoped>
.titles {
    width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    margin-bottom: 16px;
}
</style>
<template>
    <div class="item_list">
        <item></item>
        <item></item>
        <item></item>
        <item></item>
        <item></item>
        <item></item>
        <item></item>
        <item></item>
        <item></item>
        <item></item>
        <item></item>
        <item></item>
    </div>
</template>

<script>
import item from '@/components/item'
export default {
    name: 'item_list',
    components: {
        item
    }
}
</script>

<style scoped>
.item_list {
    display: flex;
    flex-wrap: wrap;
}
</style>
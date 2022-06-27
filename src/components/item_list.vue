<template>
    <div class="item_list">
        <item v-for="(p, i) in product" v-bind:p="p" v-on:remove-item="removeItem" v-bind:index="i"></item>
    </div>
</template>

<script>
import item from '@/components/item'
export default {
    props: ['product'],
    components: {
        item
    },
    methods: {
        removeItem(id) {
            this.$emit('remove-item', id)
        }
    }
}
</script>

<style scoped>
.item_list {
    display: flex;
    flex-wrap: wrap;
}
</style>
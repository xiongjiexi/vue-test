<template>
    <li>
        <slot></slot>
    </li>
</template>

<script>
export default {
    name: 'TodoList_slot',
    props: ['item'],

}
</script>

<style scoped>

</style>

<template>
    <li>
        <input type="checkbox" v-model="checked"/>
        <slot name="item" v-bind="{checked}"></slot>
    </li>
</template>

<script>
export default {
    name: 'TodoList_checkbox',
    props: ['item'],
    data() {
        return {
            checked : false
        }
    }

}
</script>

<style scoped>

</style>

<template>
    <div id='tree'>
            <ul v-for="item in child">
                    <li>{{item.label}}</li>
                    <tree v-if="item.children" :child="item.children"></tree>
            </ul>
    </div>
</template>

<script>
export default {
    name: 'tree',
    props:['child']
}
</script>

<style scoped>

</style>
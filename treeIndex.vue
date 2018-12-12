<template>
    <div id='id'>
        <ul v-for="item in data">
            <li>{{item.label}}</li>
            <tree v-if="item.children" :child="item.children"></tree>
        </ul>
        
    </div>
</template>

<script>
import tree from './treeComponent.vue'

export default {
    name: 'name',
    components: {
        tree,
    },
    data () {
        return {
            data: [{
          label: '一级 1',
          children: [{
            label: '二级 1-1',
            children: [{
              label: '三级 1-1-1'
            }]
          }]
        }, {
          label: '一级 2',
          children: [{
            label: '二级 2-1',
            children: [{
              label: '三级 2-1-1'
            }]
          }, {
            label: '二级 2-2',
            children: [{
              label: '三级 2-2-1'
            }]
          }]
        }, {
          label: '一级 3',
          children: [{
            label: '二级 3-1',
            children: [{
              label: '三级 3-1-1'
            }]
          }, {
            label: '二级 3-2',
            children: [{
              label: '三级 3-2-1'
            }]
          }]
        }]
        }
    }
    

}
</script>

<style scoped>

</style>
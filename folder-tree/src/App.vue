<template>
  <div id="app">
    <tree :data="node" v-for="node in nodes"></tree>
  </div>
</template>

<script>
import Hello from './components/Hello'
import Tree from './components/tree_ctrl.vue'

export default {
  name: 'app',
  data: function () {
    return {
      nodes: [
        {
          name: 'MaterialList',
          selected: false,
          selecting: false,
          open: true,
          path: '/MaterialList',
          floor: 1,
          type: 'folder',
          children: [
            {
              name: 'MaterialList',
              selected: false,
              selecting: false,
              open: true,
              path: '/MaterialList',
              floor: 2,
              type: 'folder',
              children: []
            },
            {
              name: 'Search Result',
              selected: false,
              selecting: false,
              open: true,
              path: '/Search Result',
              floor: 2,
              type: 'folder',
              children: []
            }
          ]
        },
        {
          name: 'Search Result',
          selected: false,
          selecting: false,
          open: true,
          path: '/Search Result',
          floor: 1,
          type: 'folder',
          children: [
            {
              name: 'MaterialList',
              selected: false,
              selecting: false,
              open: true,
              path: '/MaterialList',
              floor: 2,
              type: 'folder',
              children: []
            },
            {
              name: 'Search Result',
              selected: false,
              selecting: false,
              open: true,
              path: '/Search Result',
              floor: 2,
              type: 'folder',
              children: [
                {
                  name: 'MaterialList',
                  selected: false,
                  selecting: false,
                  open: true,
                  path: '/MaterialList',
                  floor: 3,
                  type: 'folder',
                  children: []
                },
                {
                  name: 'Search Result',
                  selected: false,
                  selecting: false,
                  open: true,
                  path: '/Search Result',
                  floor: 3,
                  type: 'folder',
                  children: []
                }
              ]
            }
          ]
        }
      ]
    }
  },
  components: {
    Hello,
    Tree
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

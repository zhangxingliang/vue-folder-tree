<template>
  <li>
    <div :title="node.name" class="folder_container" :class="{folder_selected : node.selected}" @click="click" @dblclick="dblclick" :style="{paddingLeft:20 * node.floor + 'px'}">
      <span class="folder_icon" :class="node.open ? 'icon_openned' : 'icon_closed'" @click="toggle"></span>
      <span :class="node.icon" class="folder_icon"> </span>
      <span class="folder_name">{{node.name}}</span>
    </div>
    <ul v-show="node.open">
      <tree-ctrl :data="n" v-for="n in node.children"></tree-ctrl2>
    </ul>
  </li>
</template>
<script>
export default {
  props: {
    data: Object
  },
  name: 'tree-ctrl',
  methods: {
    click: function () {
    },
    dblclick: function () {
    },
    toggle: function () {
    }
  },
  computed: {
    node () {
      return this.data
    }
  }
}
</script>
<style scoped>
ul,ol,li
{
  display: block;
  list-style-type: none;
  -webkit-margin-before: 0px;
  -webkit-margin-after: 0px;
  -webkit-margin-start: 0px;
  -webkit-margin-end: 0px;
  -webkit-padding-start: 0px;
  padding: 0;
  margin: 0;
}
.folder_container ul
{
  padding-left: 10px;
}
.folder_container
{
	background-color: #222;
  cursor: default;
  font-weight: normal;
  height: 25px;    line-height: 25px;
	font-size:12px;
	color:#cfd2d4;
	padding-left:10px;
}
.folder_container:hover
{
	background-color:#f5a623;
	color:#fff;
}
.folder_selected
{
	background-color:#f5a623;
	color:#000;
}
</style>

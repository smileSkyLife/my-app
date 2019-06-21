<template>
  <div>
    <nav-bar></nav-bar>
    <b-container>
      <draggable v-model="items" style="display: flex;flex-wrap: wrap">
        <card v-for="item in items" :key="item" :item="item"></card>
      </draggable>
      <b-row align-h="start">
        <b-col cols="4">One of two columns</b-col>
        <b-col cols="4">One of two columns</b-col>
      </b-row>

      <b-row align-h="center">
        <b-col cols="4">One of two columns</b-col>
        <b-col cols="4">One of two columns</b-col>
      </b-row>

      <b-row align-h="end">
        <b-col cols="4">One of two columns</b-col>
        <b-col cols="4">One of two columns</b-col>
      </b-row>

      <b-row align-h="around">
        <b-col cols="4">One of two columns</b-col>
        <b-col cols="4">One of two columns</b-col>
      </b-row>

      <b-row align-h="between">
        <b-col cols="4">One of two columns</b-col>
        <b-col cols="4">One of two columns</b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
	import draggable from 'vuedraggable'
	import NavBar from "./NavBar";
	import Card from './Card.vue'

	export default {
		name: "hello-vue",
		data() {
			return {
				items: ['Item 1', 'Item 2', 'Item 3', 'Item 4'],
			}
		},
		components: {
			NavBar,
			Card,
			draggable
    }
	}
</script>
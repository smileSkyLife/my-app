<template>
  <b-card
      title="Card Title"
      img-src="https://picsum.photos/600/300/?image=25"
      img-alt="Image"
      img-top
      tag="article"
      style="max-width: 20rem;"
      class="mb-2"
  >
    <b-card-text>
      {{item}}
    </b-card-text>

    <b-button variant="primary" @click="show">Go somewhere</b-button>
  </b-card>
</template>

<script>
	export default {
		name: "card",
    props: ['item'],
    methods: {
			show() {
				window.alert(this.item)
      }
    }
	}
</script>

<style scoped>

</style>
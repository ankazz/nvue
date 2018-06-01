<template>
  <div class="training">
    <h1>Math training</h1>
    <hr>
    <app-start-screen v-if="state == 'start'"></app-start-screen>
    <app-question v-else-if="state == 'question'"></app-question>
    <app-message v-else-if="state == 'message'"></app-message>
    <app-result-screen v-else-if="state == 'results'"></app-result-screen>
    <div v-else>Unkown state</div> 
  </div>
</template>

<script>
export default {
  data () {
    return {
      state: 'start'
    }
  }
}
</script>

<style scoped>
	.training{
		max-width: 700px;
		margin: 20px auto;
	}
</style>
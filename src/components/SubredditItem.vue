<template>
  <li v-on:click="handleClick">{{subreddit.data[1]}}</li>
</template>

<script>
  import {eventBus} from '../main'
export default {
  name: 'subredditItem',
  props: ['subreddit'],
  methods: {
      handleClick() {
          eventBus.$emit('subreddit-selected', this.selectedSubreddit)
      }
  }
}
</script>

<style>

</style>
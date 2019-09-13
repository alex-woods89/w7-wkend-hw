<template>
  <div id="subredditList">
       <ul>
         <subreddit-item v-for="(subreddit, index) in subreddits" :subreddit="subreddit" :key="index"></subreddit-item>  
       </ul>
  </div>
</template>

<script>
import SubredditItem from './SubredditItem'
export default {
    name: 'subreddit-list',
    props: ['subreddits'],
    components: {
      "subreddit-item": SubredditItem
    }
}
</script>

<style>

</style>
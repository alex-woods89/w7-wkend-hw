<template>
  <div id="app">
    <h1>Edinburgh subreddit app</h1>
    <subreddit-list :subreddits='subreddits'></subreddit-list>
    <subreddit-info :selectedSubreddit='selectedSubreddit'></subreddit-info>
  </div>
</template>

<script>
import {eventBus} from "./main"
import SubredditList from './components/SubredditList'
import SubredditInfo from './components/SubredditInfo'


export default {
  name: 'app',
   data() {
     return{
       subreddits: [],
       selectedSubreddit: null
     }
   },
  components: {
    "subreddit-list": SubredditList,
    "subreddit-info": SubredditInfo
  },
  mounted() {
    fetch('https://www.reddit.com/r/Edinburgh/.json')
    .then(result => result.json())
    .then(subreddits => this.subreddits = subreddits)
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

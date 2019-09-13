<template>
  <div v-if="subreddit" id ="subredditInfo">
      <h3>{{subreddit.title}}</h3>
    <li>{{subreddit.author_flair_text}}</li>
    <li>{{subreddit.likes}}</li>
     <li>{{subreddit.subreddit_subscribers}}</li>
     <li>{{subreddit.url}}</li>
  </div>
</template>

<script>
export default {
    name: 'subreddit-info',
    props:['subreddit']

}
</script>

<style>

</style>
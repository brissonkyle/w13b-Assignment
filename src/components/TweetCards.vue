<template>
    <div>
        <h2>{{usersTweets}}</h2>
        <p>{{tweetContent}}</p>
        <h5>{{dateCreated}}</h5>
    </div>
</template>

<script>
    export default {
        name : 'TweetCards',
        props: {
            usersTweets : String,
            tweetContent : String,
            dateCreated : String
        },
    }
</script>

<style lang="scss" scoped>
    div {
        color: crimson;
        border: solid 3px crimson;
        margin: 5px;
    }
</style>
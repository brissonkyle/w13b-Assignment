<template>
    <div>
        <h2>Welcome</h2>
        <div>
        <button @click="toggleButton">{{displayGridView}}</button>
        </div>
        <div :class="[ isListView ? 'listContainer' : 'gridContainer']">
        <TweetCards v-for="tweet in tweets"
        :key="tweet.dateCreated"
        :dateCreated="tweet.dateCreated"
        :usersTweets="tweet.usersTweets"
        :tweetContent="tweet.tweetContent"/>
        </div>
    </div>
</template>

<script>
import TweetCards from './TweetCards.vue'
    export default {
        components: { TweetCards,},
        name : 'TweetDisplay',
        data() {
            return {
                displayGridView : 'Switch to grid',
                isListView: true,
    
                tweets : [
                    {
                        usersTweets : 'Kyle',
                        tweetContent : 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eaque, ducimus!',
                        dateCreated : '2022,02,03',
                    },
                    {
                        usersTweets : 'Kyle',
                        tweetContent : 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eaque, ducimus!',
                        dateCreated : '2022,02,04',
                        
                    },
                    {
                        usersTweets : 'Kyle',
                        tweetContent : 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eaque, ducimus!',
                        dateCreated : '2022,02,05',
                        
                    },
                    {
                        usersTweets : 'Kyle',
                        tweetContent : 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eaque, ducimus!',
                        dateCreated : '2022,02,06',
                        
                    },
                    {
                        usersTweets : 'Kyle',
                        tweetContent : 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eaque, ducimus!',
                        dateCreated : '2022,02,07',
                        
                    },
                    {
                        usersTweets : 'Kyle',
                        tweetContent : 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eaque, ducimus!',
                        dateCreated : '2022,02,08',
                        
                    },
                ]
            }
        },
        methods: {
            toggleButton() {
                this.isListView = !this.isListView;
                if (!this.isListView) {
                    this.isListView
                    this.displayGridView = 'Switch to list View';
                    console.log('This is grid view');
                } else {
                    !this.isListView;
                    this.displayGridView = 'Switch to grid view';
                    console.log('This is list view');
                }
            }
        },
        }
</script>

<style lang="scss" scoped>
    .listContainer {
        display: block;
    }
    
    
    .gridContainer {
        box-sizing: border-box;
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-template-rows: auto;
    }

</style>
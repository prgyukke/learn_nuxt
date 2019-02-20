<template>
  <section class="container">
    <div class="form">
      <textarea cols="30" rows="10" v-model="newTweet">
      </textarea>
      <button @click="addTweet">ツイート</button>
    </div>
    <div>
      <article class="tweet row" v-for="tweet in tweets">
        <p class="col-6">
          {{ tweet.content }}
        </p>
        <p class="col-6">
          @{{ tweet.ahtuor }}
        </p>
      </article>
    </div>
  </section>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  },
  asyncData (context) {
    return {
      tweets: [
        {
          ahtuor: "foo",
          content: "first tweet",
        },
        {
          ahtuor: "bar",
          content: "second tweet",
        },
      ],
      newTweet: ""
    }
  },
  methods: {
    addTweet: function () {
      let tweet = {
        ahtuor: "hoge",
        content: this.newTweet,
      }
      this.tweets.push(tweet)
      this.newTweet = ""
    }
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>

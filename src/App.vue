<template>
  <div>
    <div class="flex justify-center mt-8">
      <img src="/images/dtv.png" width="200" height="200"/>
    </div>
    <div class="flex justify-center my-8">
      <Search @onSubmit="handleSubmit"/>
    </div>
    <div class="flex justify-center">
      <Bracket :url="url" />
    </div>
  </div>
</template>

<script>
import Search from './components/Search.vue';
import Bracket from './components/Bracket.vue';

export default {
  name: 'App',
  data() {
    return {
      url: "",
      value: ""
    };
  },
  components: {
    Search,
    Bracket,
  },
  methods: {
    handleSubmit(value) {
      this.url = `https://challonge.com/${value}/module`;
      this.value = value;
    }
  }
}
</script>

<style>
  body {
    background: linear-gradient(-45deg, #FF000D, #000000, #000000, #FF000D);
    background-size: 400% 400%;
    animation: gradient 15s ease infinite;
  }

  @keyframes gradient {
    0% {
      background-position: 0% 50%;
    }
    50% {
      background-position: 100% 50%;
    }
    100% {
      background-position: 0% 50%;
    }
}
</style>

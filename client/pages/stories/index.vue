<template>
  <div>
    <h2>{{title}}</h2>

    <p>
      {{sayHello()}}-
      <a v-bind:href="link">Google</a>
    </p>
    <p v-html="htmllink"></p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: 'my list',
      link: 'http://biggmind.com',
      htmllink: "<a href='http://google.com'>google</a>"
    };
  },
  methods: {
    sayHello() {
      return 'Hello';
    }
  },
  head() {
    return {
      title: 'Welcome To Bigg mind',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Best place for Bigg mind'
        }
      ]
    };
  }
};
</script>

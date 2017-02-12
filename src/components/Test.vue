<template>
  <div class="test">
    <p v-bind:title="msg">Message</p>
    <ul v-for="item in items">
        <li class="item">{{ item }}</li>
    </ul>
    <p v-if="seen">Show</p>
    <button v-on:click="changeVisibility">Click me</button>
  </div>
</template>


<script>

  export default {
    name: 'test',
    data () {
      return {
        msg: 'Message',
        seen: true,
        items: [1, 2, 3, 4, 5]
      }
    },
    methods: {
      changeVisibility () {
        this.seen = !this.seen
      }
    }
  }

</script>


<style>

  .item {
    list-style-type: none;
  }



</style>

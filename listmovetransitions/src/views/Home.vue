<template>
  <div id="flip-list-demo" class="demo">
    <button v-on:click="shuffle">Shuffle</button>
    <transition-group name="flip-list" tag="ul">
      <li v-for="item in items" v-bind:key="item">{{ item }}</li>
    </transition-group>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "home",
  data() {
    return {
      items: [1, 2, 3, 4, 5, 6, 7, 8, 9]
    };
  },
  methods: {
    shuffle: function() {
      this.items = _.shuffle(this.items);
    }
  }
};
</script>

<style scoped>
.flip-list-move {
  transition: transform 1s;
}
</style>
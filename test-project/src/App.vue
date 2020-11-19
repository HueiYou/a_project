
<template>
  <div>
    <h1>{{name}}</h1>
    <input type="text" v-model="myText" />
    <button type="button" @click="add()">Add</button>
    <h3>Amy Test babel</h3>
    <Menu :myList="myList" :key="myList.length"></Menu>
  </div>
</template>

<script>
  import Vue from "vue";
  import Menu from "./Menu";

  export default Vue.extend({
    data: function() {
      return {
        name: 'Hello World!',
        myText: '2',
        myList: [1,2,3]
      }
    },
    methods: {
      add () {
        if (this.myText) {
          this.myList.push(this.myText);
          // this.myText = '';
        }
      }
    },
    components: {
      Menu
    }
  });
</script>



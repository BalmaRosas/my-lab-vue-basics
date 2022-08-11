<template>
  <div class="hello">
    <!-- ITERACIÓN 2 -->
    <div id="suma">
    <p>{{ 2 + 2 }}</p>
    <p> 2+2 = {{ result }} </p>
    <!-- <p> {{operation.resultado}} </p> -->
    </div>
    <!-- ITERACIÓN 3 -->
    <div>
      <p v-if="property === true">Show me!</p>
    </div>
    <!-- ITERACIÓN 4 -->
    <div>
      <!-- <h1 v-for="post in posts" v-bind:key="post"> {{post}} </h1> -->
      <p v-for="(post, index) in posts" :key="index">
      {{post.title}} - {{post.description}} - {{post.content}}</p>
    </div>
    <!-- ITERACIÓN 5 -->
    <div>
      <h1 :class="active ? 'pink' : 'lilac'">Object of change</h1>
      <button v-on:click="changeColor" >Clik me!</button>
    </div>
    
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },

   data() {
    return {
      result: 4,

      property: true,

      posts: [
        {title: "White Sharks", description: "This post is about marine biology", content: "The great white shark (Carcharodon carcharias), also known as the white shark, white pointer, or simply great white, is a species of large mackerel shark which can be found in the coastal surface waters of all the major oceans."},
        {title: "Florida Tortoises", description: "This post is about a specific species of tortoise", content: "Gopher tortoises are long-lived reptiles that occupy upland habitat throughout Florida including forests, pastures, and yards. They dig deep burrows for shelter and forage on low-growing plants."},
        {title: "Guinea Pigs", description: "This post is about rodents", content: "The guinea pig or domestic guinea pig (Cavia porcellus), also known as the cavy or domestic cavy (/ˈkeɪvi/), is a species of rodent belonging to the genus Cavia in the family Caviidae."}
      ],

      active: false,
    }
  },

  methods: {

    changeColor() {

    },
    
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.pink {
  background-size: 100px 50px;
  background-color: rgb(250, 174, 214);
}

.lilac {
  background-size: 100px 50px;
  background-color: rgb(206, 174, 250);
}
</style>

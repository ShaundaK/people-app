<template>
  <div class="home">
    <h1>{{ message }}</h1>
    <ol>
      <li v-for="person in people">name: {{person.name}} bio: {{person.bio}} bioVisable: {{person.bioVisable}}</li>
    </ol>
    <p>name:<input type="text" v-model="newPerson.name"></p>
    <p>bio:<input type="text" v-model="newPerson.bio"></p>
    <p><button v-on:click="addPerson()">Click here to add a person</button></p>
  </div>
</template>

<style>
</style>

<script>
export default {
  data: function() {
    return {
      message: "Welcome to Vue.js!",
      people: [

      {name: "Langston Hughes", bio: "poet and novelist", bioVisable: "true"},
      {name: "Peter Pan", bio: "boy who never wants to grow up", bioVisable: "true"},
      {name: "Cardi B", bio: "reality star turned rapper", bioVisable: "true"}
      ],
      newPerson: {name: "", bio: ""}
    };    
  },
  created: function() {},
  methods: {
    addPerson: function() {
      console.log("adding a new person");
      this.people.push(this.newPerson);
    }

  },
  computed: {}
};
</script>
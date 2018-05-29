<template>
  <div class="hello">
    <h1 class="head" v-if="person.firstname && person.lastname && from">Hello {{ person.firstname }} {{ person.lastname }} From {{ from }} :)</h1>
    <h1 v-else> We don't have all the informations required to say hello :(</h1>
    <h2>Essential Links</h2>
    <ul>
      <li>
        <a
          href="http://vuejs-templates.github.io/webpack/"
          target="_blank"
        >
          Docs for This Template
        </a>
      </li>
    </ul>
    <label>Firstname : <input type="text" v-model="person.firstname"></label>
    <label>LastName : <input type="text" v-model="person.lastname"></label>
    <label>From : <input type="text" v-model="from"></label>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      person: {
        firstname: 'William',
        lastname: 'Decourty'
      },
      from:'France',
      msg: 'That\'s a wrap'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
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
.head{
  transition: all 0.3s;
}
</style>

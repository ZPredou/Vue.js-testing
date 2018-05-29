<template>
  <div>
    <table>
        <tr :key="citizen.id" v-for="citizen in citizens">
            <td >{{ citizen.firstname }}</td>
            <td>{{ citizen.lastname }}</td>           
            <td>{{ citizen.age }}</td>           
        </tr>
    </table>
    <button @click="addCitizen">Ajouter </button>
    <label v-if="counter != 1">#citizens {{counter}}</label>
  </div>
</template>

<script>
export default {
  name: 'Citizen',
  data () {
      return{
          citizens:[]
      }
    },
    methods:{
        addCitizen(){
            this.citizens.push({"firstname":"William", "lastname":"Decourty", "age":"21"});
        }
    },
    computed:{
        counter(){
            return this.citizens.length+1
        }
    },
    mounted(){}
}
</script>
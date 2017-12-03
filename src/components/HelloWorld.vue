<template>
  <div class="hello">
    <b-alert show>{{ msg }}</b-alert>

<b-container class="bv-example-row">
    <b-row v-for="row in rows" :key="row.name">  
      
        <b-col>
         <input type="text" v-model="row.name">
        </b-col>
        
        <b-col>
         <input type="text" v-model="row.job">
        </b-col>

        <b-col>
          <a @click="removeRow(row)">Remove</a>
        </b-col>
    </b-row>
    
    <div>
  <button class="button btn-primary" @click="addRow">Add row</button>
</div>
</b-container>



  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  
  data () {
    return {
      msg: 'Welcome to SDN-GP',
      rows: [
      { name: 'James Bond', job: 'spy'},
      { name: 'Goldfinger', job: 'villain'}
      ],
      counter : 0
    }
  }, 
  methods : {

    addRow: function(){
      this.rows.push({name:this.counter + 1,job:''});
    },
    removeRow: function(row){
      var index = this.rows.indexOf(row);
      console.log("index "+index)
      this.rows.splice(index, 1);
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
</style>

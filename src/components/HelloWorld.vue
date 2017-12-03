<template>
  <div class="hello">
    <b-alert show>{{ msg }}</b-alert>

<b-container class="bv-example-row">
  <b-row>
    <b-badge show>V4 Server List</b-badge>
  </b-row>
  <b-row v-for="row in v4Servers" :key="row.serverAddress">
    <b-col>
          <input type="text" v-model="row.serverAddress" size="64">
    </b-col>
    <b-col>
          <input type="text" v-model="row.prefer">
    </b-col>
    <b-col>
      <button class="button btn-primary" @click="addRow('v4')">Add row</button>
      <button class="button btn-primary" @click="removeRow(row, 'v4')">Delete row</button>
    </b-col>
  </b-row>
  <b-row>
    <b-badge show>V6 Server List</b-badge>
  </b-row>
  <b-row v-for="row in v6Servers" :key="row.serverAddress">
    <b-col>
          <input type="text" v-model="row.serverAddress" size="64">
    </b-col>
    <b-col>
          <input type="text" v-model="row.prefer">
    </b-col>
    <b-col>
      <button class="button btn-primary" @click="addRow('v6')">Add row</button>
      <button class="button btn-primary" @click="removeRow(row, 'v6')">Delete row</button>
    </b-col>
  </b-row>
  <b-row>
    <b-badge show>Prefix List</b-badge>
  </b-row>
  
  <b-row v-for="row in prefixes" :key="row.nameserverAddress">
    <b-row>
    <b-badge show>Prefix Name</b-badge>
  </b-row>
    <b-col>
          <input type="text" v-model="row.serverAddress">
    </b-col>
    <b-col>
          <input type="text" v-model="row.prefer">
    </b-col>
    <b-col>
      <button class="button btn-primary" @click="addRow('prefix')">Add row</button>
      <button class="button btn-primary" @click="removeRow(row, 'prefix')">Delete row</button>
    </b-col>
  </b-row>
</b-container>



  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  
  data () {
    return {
      msg: 'Welcome to SDN-GP',
      "v4Servers": [
        {
          "serverAddress": "123.121.12.123",
          "prefer": "No"
        }
      ],
      "v6Servers": [
        {
          "serverAddress": "2001:0db8:85a3:0000:0000:8a2e:0370:7334",
          "prefer": "Yes"
        }
      ],
      "prefixes": [
        {
          "name": "PL_SNMP_V6",
          "networks": [
            "Network1"
          ]
        }
      ],
    }
  }, 
  methods : {

    addRow: function(rowType){
      //this.rows.push({name:'',job:''})
      //console.log(rowType)
      if(rowType === 'v4')
        this.v4Servers.push({serverAddress:'',prefer:''})
      else if  (rowType === 'v6')
        this.v6Servers.push({serverAddress:'',prefer:''})
      else (rowType === 'prefix')
        this.prefixes.push({name:'',job:''})
    },
    removeRow: function(row, rowType){
      if(rowType === 'v4') {
        var index = this.v4Servers.indexOf(row)
        this.v4Servers.splice(index, 1)
      } else if(rowType === 'v6') {
        var index = this.v6Servers.indexOf(row)
        this.v6Servers.splice(index, 1)
      } else if(rowType === 'prefix') {
        var index = this.prefixes.indexOf(row)
        this.prefixes.splice(index, 1)
      }
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

<template>
  <div class="hello">
    <b-alert show>{{ msg }}</b-alert>
    <!-- <b-container fluid>
    
    </b-container> -->
    <b-container class="bv-example-row">
    <b-row>
      
        <b-col>
          <label for="input-small">V4Address:</label>
          <b-form-input v-model="text1"
                  type="text"
                  placeholder="Enter your name"></b-form-input>
        </b-col>
        <b-col>2 of 2</b-col>
    </b-row>
    <b-row>
        <b-col>1 of 3</b-col>
        <b-col>2 of 3</b-col>
        <b-col>3 of 3</b-col>
    </b-row>
</b-container>



  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to SDN-GP'
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

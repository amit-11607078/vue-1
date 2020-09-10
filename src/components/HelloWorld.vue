<template>
  <div class="hello">
    <form @submit.prevent="onSubmit">
      <input type="text" v-model="message" placeholder=""/>
      <br/>
      <br/>
      {{message1}}
      <br/>
      <br/>
      <button type="submit" >Submit</button>

      
    </form>
      
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      message: '',  // Add this line
      message1: '',
    }
  },

  // Add this section:
  methods : {
      onSubmit() {
        this.message1 = this.message.toUpperCase();
      }
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
</style>

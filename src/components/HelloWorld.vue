<template>
  <div class="hello container-fluid">
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" integrity="sha384-BVYiiSIFeK1dGmJRAkycuHAHRg32OmUcww7on3RYdg4Va+PmSTsz/K68vbdEjh4u" crossorigin="anonymous">
    <div class="upper_menu col-xs-12 row">
      top menu
    </div>
    <div class="lower_menu col-xs-12 row">
      bottom menu
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
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
.upper_menu, .lower_menu{
  position: absolute;
  text-align: left;
  font-size:200%;
  padding-left: 3%;
  background-color: black;
  color: red;
  width:100%;
  padding: 1% 3% 1% 3%;
}
.lower_menu{
  bottom: 0%;
}
</style>

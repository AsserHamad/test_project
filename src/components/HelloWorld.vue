<template>
  <div class="hello container-fluid">
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" integrity="sha384-BVYiiSIFeK1dGmJRAkycuHAHRg32OmUcww7on3RYdg4Va+PmSTsz/K68vbdEjh4u" crossorigin="anonymous">
    <div class="bg col-xs-12 row">
    </div>
    <div class="upper_menu col-xs-12 row">
      top menu
    </div>
    <div style="margin-top:7%">
      <span class="col-xs-3"></span>
      <div class="tab col-xs-6 center-block container-fluid">
        <div class="row tabs">
          <button type="button" @click="update" v-bind:class="{success : isA1}" value="a1" class="tab_btns col-xs-2"><b>tab_01</b></button>
          <button type="button" @click="update" v-bind:class="{success : isA2}" value="a2" class="tab_btns col-xs-2"><b>tab_02</b></button>
          <button type="button" @click="update" v-bind:class="{success : isA3}" value="a3" class="tab_btns col-xs-2"><b>tab_03</b></button>
          <button type="button" @click="update" v-bind:class="{success : isA4}" value="a4" class="tab_btns col-xs-2"><b>create</b></button>
        </div>
        <div class="row">
          <div class="col-xs-3 my_posts">
            <p><span style="float:left;">my posts</span> <span style="float:right;"><<<</span></p>
          </div>
        </div>
        <div class="tables">

          <div class="objs row" style="">
            <p class="col-xs-5">position</p>
            <p class="col-xs-5">project</p>
            <p class="col-xs-2">posted</p>
        </div>
        <div class="objs row" style="border-bottom: 2px dotted rgba(0,0,0,0.3)">
          <p class="col-xs-5">Director</p>
          <p class="col-xs-5">invisible enemy</p>
          <p class="col-xs-2">20 Feb 2017</p>
      </div>
      <div style="margin-top:3%;" class="">
        <p class="col-xs-2" style="text-align:left;">post text</p>
        <span class="col-xs-6"></span>
        <button type="button" class="btn" style="background-color:#948f8d;color:white;font-weight:bold;border:2px solid #c1ad97;" name="button">delete post</button>
        <button type="button" class="btn" style="background-color:#948f8d;color:white;font-weight:bold;border:2px solid #c1ad97;" name="button">update</button>
        <textarea name="name" class="form-control" rows=10></textarea>
    </div>
    </div>
      </div>
      <span class="col-xs-3"></span>
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
      msg: 'Welcome to Your Vue.js App',
      x: 1
    }
  },
  methods: {
    update : function(event){
      console.log("x was "+this.x+" and the event target is "+event.currentTarget.value);
      this.x=event.currentTarget.value;
    },
    isA1 : function(){
      return x=='a1';
    },
    isA2 : function(){
      return x=='a2';
    },
    isA3 : function(){
      return x=='a3';
    },
    isA4 : function(){
      return x=='a4';
    },
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
p, h1, h2, span, div {
  font-size:110;
  color:rgba(0,0,0,0.6);
}
.tab{
  background-color:white;
}
.success{
  font-size:400%;
}
.tables{
  padding: 3%;
}
.objs{
  text-align:left;
  border-bottom: 2px dotted rgba(0,0,0,0.3);
  font-weight: bold;
  padding-bottom: -2%;

}
.tabs{
border-top: 2px solid rgba(0,0,0,0.2);
border-bottom: 2px solid rgba(0,0,0,0.2);
}
.tab_btns{
  background-color:transparent;
  border:none;
  font-size:140%;
  color:#8d8d8d;
  padding:0.4% 1%;
}
.bg{
  position:absolute;
  background-color:rgba(0,0,0,0.1);
  height:100%;
  width:100%;
}
.my_posts{
  font-size:130%;
  padding-top:0.5%;
  padding-bottom:0.5%;
  margin-top:3%;
  border-radius:8px;
  border: 3px solid #feead3;
}
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
.tab{
  border:
}
</style>

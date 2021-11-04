<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p style = "text-transform: uppercase;">
      Please select an app from the buttons below
    </p>
    <hr style= "visibility: hidden;">
    <button class="button-style" role="button"><router-link style="color: black; text-decoration: none;" to="/">Link to App 1</router-link></button>
    <hr style= "visibility: hidden;">
    <button class="button-style" role="button"><router-link style="color: black; text-decoration: none;" to="/about">Link to App 2</router-link></button>

  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
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
root {
  background-color: blue;
}
.button-style {
  font-size: 35px;
  font-weight: 200;
  letter-spacing: 2px;
  padding: 13px 20px 13px;
  outline: 0;
  border: 2px solid black;
  cursor: pointer;
  position: relative;
  background-color: rgba(0, 0, 0, 0);
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
}

.button-style:after {
  content: "";
  background-color: #ffe54c;
  width: 100%;
  z-index: -1;
  position: absolute;
  height: 100%;
  top: 7px;
  left: 7px;
  transition: 0.2s;
}

.button-style:hover:after {
  top: 0px;
  left: 0px;
}

@media (min-width: 300px) {
  .button-style {
    padding: 13px 50px 13px;
  }
}


</style>

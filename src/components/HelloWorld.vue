<template>
  <button @click="getUserInfo">add</button>
</template>

<script>

import { apiGetUserInfo } from '../apis/user'
// import axios from "axios";

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  methods:{
    getUserInfo() {
  //   const param = {
  //   userID: '10001',
  //   userName: 'Mike',
  // }
  apiGetUserInfo().then((res) => {
    console.log(res)
  })


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

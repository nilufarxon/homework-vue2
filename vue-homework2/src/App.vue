<template>
  <div class="box">
    <h2>Sign Up</h2>
    Email : {{ email }}
    <p><input type="text" placeholder="Email" v-model="email" /></p>
    Password : {{ password }}

    <p><input type="text" placeholder="Password" v-model="password" /></p>
    <p class="error-massage" v-if="password.length < 6">
      Your password must a last 6 character
    </p>
  </div>
</template>
<script>
export default {
  data() {
    return {
      email: "",
      password: "",
    };
  },
};
</script>
<style>
* {
  margin: 0;
  padding: 0;
}
body {
  display: flex;
  justify-content: center;
  font-weight: bold;
  background: #20292c;
  color: #fff;
}
.box {
  text-align: center;
  margin-top: 50%;
  padding: 60px 20px 100px;
  border: 4px solid aquamarine;
  box-shadow: 0 5px 10px 0px rgba(7, 220, 220),
    1px 3px 4px 0px rgba(7, 220, 220);
}
.box:hover {
  border: 4px solid aqua;
  transition: 05s ease-in-out;
}
input {
  background-color: rgb(133, 244, 244);
  border: none;
  padding: 8px 15px;
  margin: 20px 0;
  width: 250px;
  border-radius: 15px;
  border-bottom: 2px solid aqua;
  box-shadow: inset 0 3px 4px rgb(55, 192, 146), 0 -1px 1px #fff, 0 1px 0 #fff;
  overflow: hidden;
  font-weight: bold;
}
input::placeholder {
  font-style: italic;
  font-weight: bold;
}

h2 {
  font-style: oblique;
  margin-bottom: 30px;
}
</style>

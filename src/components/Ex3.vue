<script>
export default {
  data() {
    return {
      loginOption: "username",
      username: "",
      email: ""
    }
  }
}

</script>

<template>
    <h1>Please select your login option</h1>
    <!-- Add/modify code in the following to have a dropdown list 
        which lets the user to select either to login with username or email -->
    <!--binds the dropdown to a Vue variable (loginOption).-->
    <select v-model="loginOption">
        <option value="username">Username login</option>
        <option value="email">Email login</option>
    </select>
    
    <div v-if="loginOption === 'username'">
        <label>Username</label>
        <input placeholder="Enter your username">
    </div>

        <div v-else>
        <label>Email</label>
        <input placeholder="Enter your email address">
    </div>
</template>


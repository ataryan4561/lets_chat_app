<template>
  <f7-page name="signup">
    <f7-navbar title="Sign Up" back-link="Back"></f7-navbar>
    <div class="wrapper">
        <img class="image--cover" :src="image_url" alt="" @click="launchFilePicker">
    </div>
    <f7-list no-hairlines-md>    

<f7-list-input :value="name" @input="name=$event.target.value"
    label="Name"
    type="text"
    placeholder="Your Name"
    clear-button
  >
  </f7-list-input>

 <f7-list-input :value="email" @input="email=$event.target.value"
    label="E-mail"
    type="email"
    placeholder="Your e-mail"
    clear-button
  >
  </f7-list-input>

  <f7-list-input :value="password" @input="password=$event.target.value"
    label="Password"
    type="password"
    placeholder="Your password"
    clear-button
  >
  </f7-list-input>

 
</f7-list>
<f7-block>
<f7-button outline>Sign Up</f7-button>
<br>
</f7-block>
  </f7-page>
</template>
<script>
export default {
  data(){
    return{
      name:null,
      email:null,
      password:null,
      image_url:'https://www.numbersia.com/sites/default/files/styles/user_detail/public/dummyUser.jpg'
    }
  }
}
</script>
<style scoped>
.wrapper {
    text-align: center;
}

.image--cover {
    width: 150px;
    height: 150px;
    border-radius: 50%;
    margin: 20px;
    object-fit: cover;
    object-position: center;
}
</style>
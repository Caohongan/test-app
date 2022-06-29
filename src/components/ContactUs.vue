<template>
  <div class="contact-us">
    <h2>Contact Us</h2>
    <div class="content-input">
        <input placeholder="Input Email" v-model="info.email" type="email"><br>
        <textarea placeholder="Input Content..." v-model="info.content" name="" id="" cols="30" rows="10"></textarea>
        <button class="button-css" @click="addItem" type="button">See all</button>
    </div>  
  </div>
</template>

<script>
export default {
  data() {
    return {
      info:{
          email: null,
          content : null,
      }
    };
  },
  mounted() {},
  methods: {
    addItem(){
        alert(this.info)
    }
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
.contact-us {
  text-align: center;
  padding: 0 300px;
  .button-css{
      background-color: rgb(72, 209, 97);
      border : 1px solid rgb(72, 209, 97);
      color: white;
      border-radius: 50px;
      padding: 10px 20px;
      float: right;
       opacity: 0.9;
      &:hover{
      
          opacity: 1;
      }
  }
  .content-input{
      padding: 0 100px;
      text-align: left;
      input{
          border: none;
          border-radius:2px;
          margin-bottom: 10px;
          height: 30px;
        width: 100%;
          background-color: #f2f2f2;
          &:focus{
              outline: none !important;
              border: white;
          }
      }
      textarea{
          border: none;
          border-radius:2px;
          margin-bottom: 10px;
          width: 100%;
          background-color: #f2f2f2;
          &:focus{
              outline: none !important;
              border: white;
          }
      }
  }

}
</style>

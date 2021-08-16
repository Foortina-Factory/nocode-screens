<template>
  <Page actionBarHidden="true">
    <GridLayout rows="*,auto">
      <StackLayout row="0" class="header-container">
        <Label text="Welcome " class="title text-primary"/>
        <Label text="Back" class="title text-primary"/>
      </StackLayout>
      
      <StackLayout row="1" class="">
        
        <StackLayout class="form-textField">
          <TextField v-model="email" keyboardType="email" class="textField" hint="Email"/>
        </StackLayout>
        
        <StackLayout class="form-textField">
          <TextField v-model="password" secure="true" class="textField" hint="Password" />
        </StackLayout>

        <GridLayout columns="auto,*,auto" marginTop="15">
          <Label col="0" text="Sign in" fontSize="20" verticalAlignment="middle" class="text-primary text-left"/>
          <Label col="2" class="btn-primary text-right fas" text.decode="&#xf061;" />
        </GridLayout>

        <GridLayout columns="auto,*,auto" marginTop="50">
          <Label col="0" text="Sign up" class="text-secondary text-left"/>
          <Label col="2" text="Forgot Passwords?" class="text-secondary text-right"/>
        </GridLayout>

      </StackLayout>
    </GridLayout>
  </Page>
</template>

<script>
  export default {
    data () {
      return {
        email: '',
        password: ''
      }
    },
    computed: {
      message() {
      return "Blank {N}-Vue app";
      }
    }
  };
</script>

<style scoped lang="scss">
  // Photo by <a href="https://unsplash.com/photos/64LL2fP9uXM">Jordan Steranka</a> 
  // design by <a href="https://dribbble.com/Tamarashvili">Giga Tamarashvili</a>
  // Market Url : https://dribbble.com/shots/6371155-Sign-in-Sign-up-UI
  
  @import '@nativescript/theme/scss/variables/blue';
  $color1: #fff;
  $color2: #000;

  Page {
    background-image: url('~/components/Login-B/bkg.jpg');
    background-size: cover;
    background-position-y: -100%;
    padding: 30;
  }

  .header-container {
    vertical-align: middle;
  }

  .title {
    font-size: 34;
    text-wrap: true;
    font-weight: 600;
  }

  .form-textField {
    margin: 10 0;
  }
  
  .textField {
    margin-left: 0;
    margin-right: 0;
    padding-bottom: 5;
    font-size: 16;
    placeholder-color: $color1;
    border-color: $color1;
    color: $color1;
    vertical-align: middle;
  }

  .text-primary {
    color: $color1;
  }

  .text-secondary {
    text-decoration: underline;
    text-decoration-color: $color1;
    color: $color1;
    font-size: 16;
  }

  .btn-primary {
    background-color: $color1;
    color: $color2;
    border-radius: 100%;
    z-index: 0;
    font-size: 18;
    text-align: center;
    width: 64;
    height: 64;
    vertical-align: middle;
    padding: 22 0;
  }
</style>

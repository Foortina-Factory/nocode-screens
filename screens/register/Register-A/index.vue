<template>
  <Page actionBarHidden="true">
    <GridLayout rows="auto, *, auto">
      <Image row="0" src="~/components/Login-A/logo.png" class="logo"/>
      <StackLayout row="2" class="auth-box">
        <Label text="New Account" class="title"/>
        
        <StackLayout class="form-textField">
          <Label text="Email" class="form-label"/>
          <GridLayout class="">
            <Label class="fas form-icon" text.decode="&#xf0e0;"/>
            <TextField v-model="email" class="textField"/>
          </GridLayout>
        </StackLayout>

        <StackLayout class="form-textField">
          <Label text="Username" class="form-label"/>
          <GridLayout class="">
            <Label class="fas form-icon" text.decode="&#xf007;"/>
            <TextField v-model="username" class="textField"/>
          </GridLayout>
        </StackLayout>
        
        <StackLayout class="form-textField">
          <Label text="Password" class="form-label"/>
          <GridLayout class="">
            <Label class="fas form-icon" text.decode="&#xf084;"/>
            <TextField v-model="password" class="textField"/>
          </GridLayout>
        </StackLayout>

        <Button class="btn-primary" text="Sign up"/>
      </StackLayout>
    </GridLayout>
  </Page>
</template>

<script>
  export default {
    data () {
      return {
        email: '',
        username: '',
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
  //Photo by <a href="https://unsplash.com/@heycrisso?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Chris Galbraith</a> on <a href="https://unsplash.com/wallpapers/nature/beach?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>
  
  @import '@nativescript/theme/scss/variables/blue';
  $color1: #FE7F55;
  $color2: #fff;
  $color3: #777;

  Page {
    background-image: url('~/components/Register-A/bkg.jpg');
    background-size: cover;
    background-position-y: -100%;
  }

  .logo {
    width: 200;
    margin-top: 100;
    margin-left: 35;
    horizontal-align: left;
  }

  .auth-box {
    background: #fff;
    padding: 30 30;
    border-top-right-radius: 40;
    border-top-left-radius: 40;
    box-shadow: 0 0 6 rgba(40, 40, 40, 0.7);
  }

  .title {
    font-size: 28;
    text-wrap: true;
    margin-bottom: 20;
    font-weight: 700;
  }

  .form-textField {
    margin: 10 0 10;
  }

  .form-label {
    font-size: 12;
    color: $color3;
  }
  
  .form-icon {
    font-size: 16;
    vertical-align: bottom;
    margin-bottom: 10;
    color: $color3;
  }
  
  .textField {
    margin-left: 0;
    margin-right: 0;
    padding-left: 24;
    padding-bottom: 5;
    font-size: 16;
    border-color: $color1;
  }

  .text-primary {
    margin-top: 10;
    color: $color1;
  }

  .btn-primary {
    background-color: $color1;
    color: $color2;
    border-radius: 100%;
    z-index: 0;
    font-size: 16;
    margin: 20 0 20;
  }
</style>

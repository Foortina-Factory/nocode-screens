<template>
  <Page actionBarHidden="true">
    <ScrollView>
      <GridLayout class="container" rows="*,auto" height="100%">
        <StackLayout class="header-container" row="0">
          <Label text="Create" class="title" />
          <Label text="Account" class="title" />
        </StackLayout>
        <GridLayout class="footer-container" row="1" rows="auto,10,auto,10,auto,15,auto,auto,auto">
          <GridLayout row="0" columns="auto,*,auto" class="form-textField">
            <Label col="0" class="form-icon fas " text.decode="&#xf007; " />
            <TextField col="1" v-model="user.name" class="textField"
              hint="Jonh Doe" />
          </GridLayout>

          <GridLayout row="2" columns="auto,*,auto" class="form-textField">
            <Label col="0" class="form-icon fas " text.decode="&#xf0e0; " />
            <TextField col="1" v-model="user.email" keyboardType="email" class="textField"
              hint="beaud@foortina.com" />
          </GridLayout>

          <GridLayout row="4" columns="auto,*,auto" class="form-textField">
            <Label col="0" class="form-icon fas " text.decode="&#xf023;" />
            <TextField col="1" v-model="user.password" :secure="secure" class="textField"
              hint="Password" />
            <Label col="2" class="form-icon fas " text.decode="&#xf070;" @tap="secure = !secure" />
          </GridLayout>

          <Label row="6" text="Sign up" textWrap="true" class="btn-primary" />

          <GridLayout row="7" columns="*,auto,*" class="" verticalAlignement="middle">
            <StackLayout col="0" height="1" class="hr" verticalAlignement="middle"></StackLayout>
            <Label col="1" class="text-secondary" text="or" fontSize="20" margin="0 8" padding="0 0 8" />
            <StackLayout col="2" height="1" class="hr" verticalAlignement="middle"></StackLayout>
          </GridLayout>

          <Label row="8" text="Login" textWrap="true" class="btn-secondary" />

        </GridLayout>
      </GridLayout>
    </ScrollView>
    
  </Page>
</template>
<script>

  export default {
    data() {
      return {
        user: {
          name: '',
          email: '',
          password: ''
        },
        secure: true,
      };
    },
  };
</script>

<style scoped lang="scss">
// design by <a href="https://dribbble.com/liliyakizlaitis">Liliya Kizlaitis</a>
// Market Url : https://dribbble.com/shots/7861676-Sign-in-Sign-up-UI/attachments/483139?mode=media

	@import '@nativescript/theme/scss/variables/blue';

  $color1: #006bff;
  $color2: #fff;
  $color3: #888;
  
	.fas {
    vertical-align: middle;
		@include colorize($color: #0059D4);
	}

  .container {
    background-color: $color1;
    background-image: url('~/components/Register-C/bkg.jpg');
    background-size: cover;
  }

  .header-container {
    padding: 20;
    vertical-align: middle;
    // background-image: url('~/components/Login-C/bkg.jpeg');
  }

  .title {
    text-align: left;
    color: $color2;
    font-size: 28;
    vertical-align: middle;
    font-style: italic;
  }

  .footer-container {
    padding: 20;
    background-color: $color2;
  }

  .form-textField {
    border-bottom-width: 1;
    border-bottom-color: $color3;
    margin: 8 0;
    height: 40;
    color: $color3;
    font-size: 16;
    padding: 0 2;
  }
  
  .form-icon {
    vertical-align: middle;
  }

  .hr {
    color: $color1;
    vertical-align: middle;
  }

  .text-secondary {
    color: $color3;
  }

  .textField {
    border-bottom-width: 0;
    border-bottom-color: $color2;
    font-size: 15;
    placeholder-color: $color3;
    font-weight: 400;
  }

  .btn-primary {
    background-color: $color1;
    color: $color2;
    padding: 10;
    text-align: center;
    border-radius: 6;
    font-size: 15;
  }

  .btn-secondary {
    background-color: $color2;
    color: $color3;
    padding: 10;
    text-align: center;
    border-radius: 6;
    font-size: 15;
    border-width: 1;
    border-color: $color3;
  }

</style>

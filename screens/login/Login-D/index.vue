<template>
	<Page actionBarHidden="true">
    <GridLayout class="container" rows="*,auto" height="100%">
      <StackLayout class="header-container" row="0">
        <Image src="~/components/Login-D/img.png" class="header-img" />
      </StackLayout>
      <GridLayout class="footer-container" row="1" rows="auto,20,auto,auto,15,auto,15,auto,15,auto,15,auto">
        <Label row="0" text="Login" class="title" />
        
        <GridLayout row="2" columns="auto,*,auto" class="form-textField">
          <Label col="0" class="form-icon fas" text="@" />
          <TextField col="1" v-model="user.email" keyboardType="email" class="textField"
            hint="Email ID" />
        </GridLayout>

        <GridLayout row="3" columns="auto,*,auto" class="form-textField">
          <Label col="0" class="form-icon fas " text.decode="&#xf023;"  />
          <TextField col="1" v-model="user.password" secure="true" class="textField"
            hint="Password" />
          <Label col="2" class="font-weight text-primary" text="Forgot?" textWrap="true" />
        </GridLayout>

        <Label row="5" text="Login" textWrap="true" class="btn-primary" />

        <Label row="7" class="text-secondary font-weight text-center" text="Or, login with..." textWrap="true" />

        <GridLayout row="9" columns="*,10,*,10,*" class="" verticalAlignement="middle">
          <Label col="O" class="box-network fab" text.decode="&#xf1a0;"  />
          <Label col="2" class="box-network text-primary fab" text.decode="&#xf09a;"  />
          <Label col="4" class="box-network fab" text.decode="&#xf179;"  />
        </GridLayout>

        <Label class="text-center" row="11">
          <FormattedString class="text-center" fontSize="14">
            <Span  text="New to Foortina Factory? "/>
            <Span class="text-primary" text="Register"/>
          </FormattedString>
        </Label>

      </GridLayout>
    </GridLayout>
	</Page>
</template>

<script>
  export default {
    data() {
      return {
        user: {
          email: '',
          password: ''
        },
        secure: true,
      };
    },
    computed: {
      message() {
        return "Blank {N}-Vue app";
      }
    },
  };

</script>

<style scoped lang="scss">
// design by <a href="https://dribbble.com/ashwithkotian">Liliya Kizlaitis</a>Ashwith Kotian
// Market Url : https://dribbble.com/shots/14605167/attachments/6297430?mode=media

	@import '@nativescript/theme/scss/variables/blue';
  @import '@nativescript/theme/core';
  @import '@nativescript/theme/default';

  $color1: #0059D4;
  $color2: #fff;
  $color3: #888;
  
	.fas {
    vertical-align: middle;
		@include colorize($color: #0059D4);
	}

  .fab {
    font-family: 'Font Awesome 5 Brands', 'fa-brands-400';
    font-weight: 400;
  }

  .container {
    background-color: $color2;
  }

  .header-img {
    margin: 50 0 10;
    // height: 180;
    text-align: center;
  }

  .header-container {
    padding: 20;
    vertical-align: middle;
  }

  .title {
    text-align: left;
    color: black;
    font-size: 30;
    font-weight: bold;
  }

  .footer-container {
    padding: 20;
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
    font-size: 16;
    vertical-align: middle;
  }

  .text-primary {
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
    border-radius: 8;
    font-size: 15;
  }

  .box-network {
    padding: 10;
    text-align: center;
    border-radius: 8;
    font-size: 16;
    border-width: 1;
    border-color: $color3;
  }

</style>

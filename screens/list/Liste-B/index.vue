<template>
	<Page actionBarHidden="true">
    <StackLayout class="container">
      <Label text="Hi Chryzal," marginTop="14" class="title" />
      <Label text="Find your Dream Job" class="title" />

      <GridLayout columns="auto,10,*" class="search-container">
        <Label col="0" fontSize="16" class="fas jobs-icon" text.decode="&#xf002;" />
        <TextField col="2" class="textField" hint="Search for job title" />
      </GridLayout>

      <Label text="Recent Jobs" marginTop="15" class="min-title" />
      
      <ScrollView marginTop="12" orientation="vertical">
        <StackLayout orientation="vertical">
         
          <GridLayout columns="auto,10,*,10,auto" class="jobs-card">
            <Label col="0" class="fab jobs-company-default" backgroundColor="#1a73eb" text.decode="&#xf39e;"/>
            <GridLayout col="2" rows="auto,auto">
              <Label row="0" text="Senior Data Engineer" class="jobs-title" />
              <Label row="1" text="Facebook • Part time" class="jobs-subtitle" />
            </GridLayout>
            <Label col="4" class="fas jobs-icon" text.decode="&#xf142;"/>
          </GridLayout>

          <GridLayout columns="auto,10,*,10,auto" class="jobs-card">
            <Label col="0" class="fab jobs-company-secondary" text.decode="&#xf1a0;"/>
            <GridLayout col="2" rows="auto,auto">
              <Label row="0" text="Senior Mobile Engineer" class="jobs-title" />
              <Label row="1" text="Google • Full time" class="jobs-subtitle" />
            </GridLayout>
            <Label col="4" class="fas jobs-icon" text.decode="&#xf142;"/>
          </GridLayout>

          <GridLayout columns="auto,10,*,10,auto" class="jobs-card">
            <Label col="0" class="fab jobs-company-default" backgroundColor="#ef9633" text.decode="&#xf270;"/>
            <GridLayout col="2" rows="auto,auto">
              <Label row="0" text="Senior UI/UX Designer" class="jobs-title" />
              <Label row="1" text="Amazon • Contract" class="jobs-subtitle" />
            </GridLayout>
            <Label col="4" class="fas jobs-icon" text.decode="&#xf142;"/>
          </GridLayout>

          <GridLayout columns="auto,10,*,10,auto" class="jobs-card">
            <Label col="0" class="fas jobs-company-secondary" color="#d60909" borderColor="#d60909" text.decode="&#xf19c;"/>
            <GridLayout col="2" rows="auto,auto">
              <Label row="0" text="Senior Full-Stack Developer" class="jobs-title" />
              <Label row="1" text="UCAO Benin • Full time" class="jobs-subtitle" />
            </GridLayout>
            <Label col="4" class="fas jobs-icon" text.decode="&#xf142;"/>
          </GridLayout>

          <GridLayout columns="auto,10,*,10,auto" class="jobs-card">
            <Label col="0" class="jobs-company-default" backgroundColor="#45cfdb" fontSize="12" text="Foo."/>
            <GridLayout col="2" rows="auto,auto">
              <Label row="0" text="Senior UI Designer" class="jobs-title" />
              <Label row="1" text="Foortina • Remote" class="jobs-subtitle" />
            </GridLayout>
            <Label col="4" class="fas jobs-icon" text.decode="&#xf142;"/>
          </GridLayout>

          <GridLayout columns="auto,10,*,10,auto" class="jobs-card">
            <Label col="0" class="fab jobs-company-default" backgroundColor="#20d663" text.decode="&#xf1bc;"/>
            <GridLayout col="2" rows="auto,auto">
              <Label row="0" text="Senior Data Miner" class="jobs-title" />
              <Label row="1" text="Spotify • Contract" class="jobs-subtitle" />
            </GridLayout>
            <Label col="4" class="fas jobs-icon" text.decode="&#xf142;"/>
          </GridLayout>

          <GridLayout columns="auto,10,*,10,auto" class="jobs-card">
            <Label col="0" class="fab jobs-company-default" backgroundColor="#0182df" text.decode="&#xf1ed;"/>
            <GridLayout col="2" rows="auto,auto">
              <Label row="0" text="2 Junior Game Developers" class="jobs-title" />
              <Label row="1" text="Paypal • Part time" class="jobs-subtitle" />
            </GridLayout>
            <Label col="4" class="fas jobs-icon" text.decode="&#xf142;"/>
          </GridLayout>

        </StackLayout>
      </ScrollView>

    </StackLayout>
   </Page>
</template>

<style scoped lang="scss">
// Inspired by the Market : https://dribbble.com/shots/11893551-Job-Finder-Mobile-App-Screens/attachments/3519160?mode=media
	@import '@nativescript/theme/scss/variables/blue';

  $color1: #eee;
  $color2: #fff;
  $color3: #000;
  $color4: #888;

	.fas {
    vertical-align: middle;
		@include colorize($color: #0059D4);
	}

  .fab {
    font-family: 'Font Awesome 5 Brands', 'fa-brands-400';
    vertical-align: middle;
    font-weight: 400;
  }

  .container {
    background-color: $color1;
    padding: 4 20;
  }

  .search-container {
    padding: 5 8;
    border-radius: 8;
    background-color: $color2;
    color: $color3;
    height: 50;
    margin-top: 14;
  }

  .textField {
    margin-left: 0;
    margin-right: 0;
    font-size: 16;
    border-color: $color2;
    placeholder-color: $color4;
  }

  .jobs-card {
    border-radius: 8;
    padding: 10;
    margin: 4 0;
    background-color: $color2;
  }

  .jobs-title {
    color: $color3;
    font-size: 18;
    font-weight: bold;
  }

  .jobs-subtitle {
    color: $color4;
    font-size: 12;
  }

  .jobs-icon {
    color: $color3;
  }

  .title {
    text-align: left;
    color: $color3;
    font-size: 28;
  }

  .min-title {
    font-size: 18;
    color: $color3;
  }

  .tasks-card {
    border-radius: 8;
    padding: 10;
    background-color: $color1;
    margin-bottom: 8;
  }
  
  .jobs-company-primary {
    background-color: $color3;
    color: $color2;
    padding: 10 6;
    text-align: center;
    border-radius: 6;
    border-width: 1;
    border-color: $color4;
    width: 40;
    height: 40;
    vertical-align: middle;
  }

  .jobs-company-secondary {
    background-color: $color2;
    color: $color3;
    padding: 10 6;
    text-align: center;
    border-radius: 6;
    border-width: 1;
    border-color: $color4;
    width: 40;
    height: 40;
    vertical-align: middle;
    font-size: 15;
  }

  .jobs-company-default {
    padding: 10 6;
    text-align: center;
    border-radius: 6;
    width: 40;
    height: 40;
    vertical-align: middle;
    font-size: 15;
    color: $color2;
  }


</style>

<template>
	<Page >
    <ActionBar>
			<Label text="My courses"/>
		</ActionBar>
    <StackLayout class="container">
      <Label text="Wellcome back, Chryzal" marginTop="8" class="title" />

      <GridLayout columns="auto,10,*" class="search-container">
        <Label col="0" fontSize="16" class="fas jobs-icon" text.decode="&#xf002;" />
        <TextField col="2" class="textField" hint="Search for a course" />
      </GridLayout>

      <ScrollView marginTop="15" orientation="horizontal">
        <StackLayout orientation="horizontal">
          <Label text="All" class="categories-card-primary" />
          <Label text="Web Design" class="categories-card-secondary" />
          <Label text="Marketing" class="categories-card-secondary" />
          <Label text="AI" class="categories-card-secondary" />
          <Label text="Blockchain" class="categories-card-secondary" />
        </StackLayout>
      </ScrollView>
      
      <ScrollView marginTop="12" orientation="vertical">
        <StackLayout orientation="vertical">
         
          <StackLayout class="courses-card">
            <GridLayout columns="*,auto">
              <StackLayout col="0">
                <Label text="Intro to Machine Learning" textWrap="true" class="courses-title" />
                <Label class="courses-description" textWrap="true"
                  text="Learn the core ideas in machine learning, and build your first models." />
              </StackLayout>
              <Label col="1" text="$ 240" class="courses-price" />
            </GridLayout>
            <StackLayout marginTop="10" orientation="horizontal">
              <Label class="fas courses-icon" text.decode="&#xf017;"/>
              <Label text=" 5 Days"/>
            </StackLayout>
            <StackLayout orientation="horizontal">
              <Label class="fab courses-icon" text.decode="&#xf167;"/>
              <Label text="7 Lessons"/>
            </StackLayout>
          </StackLayout>

          <StackLayout class="courses-card">
            <GridLayout columns="*,auto">
              <StackLayout col="0">
                <Label text="Adobe Illustrator for Graphic Design" textWrap="true" class="courses-title" />
                <Label class="courses-description" textWrap="true"
                  text="Learn how to use Illustrator to develop any graphic design project from scratch" />
              </StackLayout>
              <Label col="1" text="$ 24" class="courses-price" />
            </GridLayout>
            <StackLayout marginTop="10" orientation="horizontal">
              <Label class="fas courses-icon" text.decode="&#xf017;"/>
              <Label text=" 10 Days"/>
            </StackLayout>
            <StackLayout orientation="horizontal">
              <Label class="fab courses-icon" text.decode="&#xf167;"/>
              <Label text="6 Lessons"/>
            </StackLayout>
          </StackLayout>

          <StackLayout class="courses-card">
            <GridLayout columns="*,auto">
              <StackLayout col="0">
                <Label text="Python" textWrap="true" class="courses-title" />
                <Label class="courses-description" textWrap="true"
                  text="Learn the most important language for data science." />
              </StackLayout>
              <Label col="1" text="$ 190" class="courses-price" />
            </GridLayout>
            <StackLayout marginTop="10" orientation="horizontal">
              <Label class="fas courses-icon" text.decode="&#xf017;"/>
              <Label  text=" 15 Days"/>
            </StackLayout>
            <StackLayout orientation="horizontal">
              <Label class="fab courses-icon" text.decode="&#xf167;"/>
              <Label text="17 Lessons"/>
            </StackLayout>
          </StackLayout>

          <StackLayout class="courses-card">
            <GridLayout columns="*,auto">
              <StackLayout col="0">
                <Label text="Intermediate to Machine Learning" textWrap="true" class="courses-title" />
                <Label class="courses-description" textWrap="true"
                  text="Handle missing values, non-numeric values, data leakage, and more." />
              </StackLayout>
              <Label col="1" text="$ 580" class="courses-price" />
            </GridLayout>
            <StackLayout marginTop="10" orientation="horizontal">
              <Label class="fas courses-icon" text.decode="&#xf017;"/>
              <Label text=" 15 Days"/>
            </StackLayout>
            <StackLayout orientation="horizontal">
              <Label class="fab courses-icon" text.decode="&#xf167;"/>
              <Label text="14 Lessons"/>
            </StackLayout>
          </StackLayout>

        </StackLayout>
      </ScrollView>

    </StackLayout>
   </Page>
</template>

<style scoped lang="scss">
	@import '@nativescript/theme/scss/variables/blue';

  $color1: #eee;
  $color2: #fff;
  $color3: #000;
  $color4: #888;
  $color5: #1452a8;


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

  .courses-card {
    border-radius: 8;
    padding: 10;
    margin: 4 0;
    background-color: $color2;
  }

  .courses-title {
    color: $color5;
    font-size: 18;
    font-weight: bold;
  }

  .courses-description {
    color: $color4;
    font-size: 12;
  }

  .courses-price {
    border-color: $color3;
    border-radius: 8;
    border-width: 1;
    color: $color3;
    background-color: $color2;
    padding: 8 5;
    text-align: center;
    vertical-align: middle;

    width: 50;
    height: 50;
  }

  .courses-icon {
    color: $color5;
    margin-right: 5;
  }

  .title {
    text-align: left;
    color: $color3;
    font-size: 22;
  }

  .min-title {
    font-size: 18;
    color: $color3;
  }

  .categories-card-primary {
    border-radius: 8;
    padding: 10;
    background-color: $color4;
    color: $color2;
    margin-right: 8;
  }

  .categories-card-secondary {
    border-radius: 8;
    padding: 10;
    background-color: $color2;
    color: $color5;
    margin-right: 8;
  }
  

</style>

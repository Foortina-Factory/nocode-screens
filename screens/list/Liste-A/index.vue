<template>
	<Page>
    <ActionBar>
			<Label text="To Do List"/>
		</ActionBar>
    <GridLayout rows="auto,auto,40,auto,auto" class="container">
      <GridLayout row="0" marginTop="6" columns="auto,*,auto">
        <Label col="0" text="CATEGORIES" class="min-title" />
        <Label col="2" class="fas btn-add" text.decode="&#xf067;" />
      </GridLayout>
      
      <ScrollView row="1" marginTop="6" orientation="horizontal">
        <StackLayout orientation="horizontal">
         
         <StackLayout class="categories-card">
          <Label text="40 tasks" class="categories-tasks" />
          <Label text="Business" class="categories-title" />
          <Progress marginTop="10" color="#cf3f63" :value="40" :maxValue="100" />
         </StackLayout>

         <StackLayout class="categories-card">
          <Label text="10 tasks" class="categories-tasks" />
          <Label text="Personal" class="categories-title" />
          <Progress marginTop="10" color="#2970ce" :value="80" :maxValue="100" />
         </StackLayout>

         <StackLayout class="categories-card">
          <Label text="5 tasks" class="categories-tasks" />
          <Label text="Domestic" class="categories-title" />
          <Progress marginTop="10" color="#42cc8c" :value="40" :maxValue="100" />
         </StackLayout>

        </StackLayout>
      </ScrollView>

      <GridLayout row="3" columns="auto,*,auto">
        <Label col="0" text="TASKS" class="min-title" />
        <Label col="2" class="fas btn-add" text.decode="&#xf067;" />
      </GridLayout>
      
      <ScrollView row="4" marginTop="12" orientation="vertical">
        <StackLayout orientation="vertical">
         
         <GridLayout columns="auto,10,*" class="tasks-card">
            <Label col="0" class="fas tasks-icon" color="#cf3f63" text.decode="&#xf1ce;"/>
            <Label col="2" text="Start the e-commerce project" class="min-title" />
         </GridLayout>

         <GridLayout columns="auto,10,*" class="tasks-card">
            <Label col="0" class="fas tasks-icon" color="#2970ce" text.decode="&#xf058;"/>
            <Label col="2" text="Check emails " class="min-title text-crossed" />
         </GridLayout>

         <GridLayout columns="auto,10,*" class="tasks-card">
            <Label col="0" class="fas tasks-icon" color="#42cc8c" text.decode="&#xf1ce;"/>
            <Label col="2" text="Feeding and drinking to the cat" class="min-title" />
         </GridLayout>

         <GridLayout columns="auto,10,*" class="tasks-card">
            <Label col="0" class="fas tasks-icon" color="#cf3f63" text.decode="&#xf058;"/>
            <Label col="2" text="Daily meeting with the team" class="min-title text-crossed" />
         </GridLayout>

         <GridLayout columns="auto,10,*" class="tasks-card">
            <Label col="0" class="fas tasks-icon" color="#42cc8c" text.decode="&#xf1ce;"/>
            <Label col="2" text="Take out the trash" class="min-title" />
         </GridLayout>

         <GridLayout columns="auto,10,*" class="tasks-card">
            <Label col="0" class="fas tasks-icon" color="#2970ce" text.decode="&#xf1ce;"/>
            <Label col="2" text="Buy a new car" class="min-title" />
         </GridLayout>

         <GridLayout columns="auto,10,*" class="tasks-card">
            <Label col="0" class="fas tasks-icon" color="#2970ce" text.decode="&#xf1ce;"/>
            <Label col="2" text="Recharge my credit card" class="min-title" />
         </GridLayout>

         <GridLayout columns="auto,10,*" class="tasks-card">
            <Label col="0" class="fas tasks-icon" color="#cf3f63" text.decode="&#xf058;"/>
            <Label col="2" text="Assist the product manager" class="min-title text-crossed" />
         </GridLayout>

         <GridLayout columns="auto,10,*" class="tasks-card">
            <Label col="0" class="fas tasks-icon" color="#42cc8c" text.decode="&#xf058;"/>
            <Label col="2" text="Sort recyclable waste" class="min-title text-crossed" />
         </GridLayout>

         <GridLayout columns="auto,10,*" class="tasks-card">
            <Label col="0" class="fas tasks-icon" color="#2970ce" text.decode="&#xf058;"/>
            <Label col="2" text="Pay the gardener" class="min-title text-crossed" />
         </GridLayout>

        </StackLayout>
      </ScrollView>

    </GridLayout>
   </Page>
</template>

<style scoped lang="scss">
// Inspired by the Market : https://dribbble.com/shots/14153121-ToDo-App-Dark-Theme/attachments/5779436?mode=media
	@import '@nativescript/theme/scss/variables/blue';

  $color1: #031956;
  $color2: #fff;
  $color3: #ddd;
  $color4: #afadad;

	.fas {
    vertical-align: middle;
		@include colorize($color: #0059D4);
	}

  .container {
    background-color: #4b5980;
    padding: 4 20;
  }

  .categories-card {
    border-radius: 8;
    padding: 10;
    margin: 8 8 8 0;
    background-color: $color1;
    width: 140;
  }

  .categories-title {
    color: $color2;
    font-size: 20;
    font-weight: bold;
  }

  .categories-tasks {
    color: $color3;
    font-size: 14;
  }

  .title {
    text-align: left;
    color: $color2;
    font-size: 28;
    vertical-align: middle;
    font-style: italic;
  }

  .min-title {
    font-size: 18;
    color: $color2;
  }

  .tasks-card {
    border-radius: 8;
    padding: 12;
    background-color: $color1;
    margin-bottom: 10;
  }
  
  .tasks-icon {
    vertical-align: middle;
    font-size: 16;
  }

  .text-crossed {
    text-decoration: line-through;
  }

  .btn-add {
    background-color: $color1;
    color: $color2;
    padding: 8 10;
    text-align: center;
    border-radius: 6;
  }

</style>

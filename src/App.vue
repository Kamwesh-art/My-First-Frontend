
<template>
  <v-app>
    <v-main>
      <HelloWorld />
      <h1>Hello {{name}}!</h1>
      <h2>Hope that u r well</h2>
      <StudentCard 
      :name="name" 
      :course="course"
      :age="age"/>
    
        <v-btn @click="changeName">
          Change My Name
        </v-btn>
        <v-btn @click="becomeSteve">
          Become Steve 
        </v-btn>
        <v-btn @click="becomeKamwesh">
          Become Kamwesh
        </v-btn>

      <h2>I am studying {{ course }}</h2>
      <h2>I am {{ age }} years old</h2>
       <v-text-field
        label="Enter your name"
        variant="solo"
        v-model="name"
        ></v-text-field>

        <v-text-field
        label="Enter course name"
        variant="filled"
        v-model="course">
        </v-text-field>

        <v-text-field
        label="Enter your age"
        variant="outlined"
        v-model="age">
      </v-text-field>

        <v-btn variant="elevated">Elevated</v-btn>
        <v-btn variant="flat">Flat</v-btn>
        <v-btn variant="tonal">Tonal</v-btn>
        <v-btn variant="outlined">Outlined</v-btn>
        <v-btn variant="text" >Text</v-btn>
        <v-btn variant="plain">Plain</v-btn>

    </v-main>
    <v-btn
      class="ma-2"
      icon="mdi-theme-light-dark"
      location="top right"
      position="absolute"
      @click="$vuetify.theme.cycle()"
    />


  </v-app>
</template>

<script lang="ts" setup>
  import HelloWorld from '@/components/HelloWorld.vue'
  import {ref} from 'vue'
  import StudentCard from '@/components/StudentCard.vue'

  const name=ref("Darling")
  function changeName() {
  name.value = "Honey "
}
  function becomeSteve(){
    console.log("The button become Steve was clicked ")
    name.value = "Steve"
  }
  function becomeKamwesh(){
    console.log("The button become Kamwesh was clicked ")
    name.value = "Kamwesh"
  }
  console.log(name)
  console.log(name.value)
  // const course="Vue and Vuetify."

  const course=ref("BBIT")
  console.log(course.value)
  const age=ref(20)
  console.log(age.value)
</script>
<style> 
h1
{
  color:blue;
  text-align:center;
}
</style>

<template>
  <v-app>
    <v-main>
      <HelloWorld />
      <h1>Hello {{name}}!</h1>
      <StudentCard 
      :name="name" 
      :course="course"
      :age="age"/>
      
      <h2>Hope that u r well</h2>
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
      <!-- <StudentCard />       -->
       <v-text-field
        label="Enter your name"
        v-model="name"
        ></v-text-field>

        <v-text-field
        label="Enter course name"
        v-model="course">
        </v-text-field>

        <v-text-field
        label="Enter your age"
        v-model="age">
      </v-text-field>

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
    console.log("The button become Steve was cicked ")
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
  const age=ref(20)
</script>
<style> 
h1
{
  color:blue;
}
</style>
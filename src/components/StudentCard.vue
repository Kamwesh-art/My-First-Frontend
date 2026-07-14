<template>
    <div>
        <h2>Student Profile</h2>
        <p>Name: {{name}} </p>
        <p>Course: {{course}}</p>
        <p>Age: {{age}}</p>
    </div>

</template>
<script setup lang="ts">

const props = defineProps({
    name: String,
    course: String,
    age: Number,
})


</script>
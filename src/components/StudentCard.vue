<template>
    <div>
        <h2>Student Profile</h2>
        <p>Name: {{props.name}} </p>
        <p>Course: {{props.course}}</p>
        <p>Age: {{props.age}}</p>
    </div>

</template>
<script setup lang="ts">

const props = defineProps({
    name: String,
    course: String,
    age: Number,
})

</script>
<template>
  <div>
    <AddStudent />
    <h3>All Students </h3>
    <div class="student-row">
      <h4>Name</h4>
      <h4>Email</h4>
      <h4>Phone</h4>
      <h4>DateOfBirth</h4>
    </div>
    <div v-bind:key="student.id" class="student" v-for="student in students">
      <p>{{ student.name }}</p>
      <p>{{ student.email }}</p>
      <p>{{ student.phone }}</p>
      <p>{{ student.dateOfBirth }}</p>
    </div>
  </div>
</template>

<script>
    import AddStudent from './AddStudent.vue';

    export default {
        name: "Students",
        props: ["students"],
        components: {
            AddStudent,
         }
    };
</script>

<style scoped>
    .student-row {
        display: flex;
        justify-content: space-around;
    }
    .student {
        display: flex;
        justify-content: space-around;
        background-color: gray;
    }
</style>

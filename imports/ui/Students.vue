<template>
  <div>
    <div class="student-row">
      <h4>Name</h4>
      <h4>Email</h4>
      <h4>Phone</h4>
      <h4>DateOfBirth</h4>
    </div>
    <div class="student" v-for="student in students">
      <p>{{ student.name }}</p>
      <p>{{ student.email }}</p>
      <p>{{ student.phone }}</p>
      <p>{{ student.DateOfBirth }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Students",
  props: ["students"],
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

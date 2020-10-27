<template>
    <div>
       <AddSubject />
       <h3>All Subjects..</h3>
       <div class="subject-row">
       <h4>Name</h4>
    </div>
    <div v-bind:key="subject.id" class="subject" v-for="subject in subjects">
      <p>{{ subject.name }}</p>
    </div>
    </div>
</template>

<script>
import AddSubject from "../components/AddSubject.vue";

export default {
    name: "Subjects",
    props:["subjects"],
    components: {
          AddSubject,
        }
}
</script>

<style scoped>
   .subjects-row {
        display: flex;
        justify-content: space-around;
    }
    .subject {
        display: flex;
        justify-content: space-around;
        background-color: gray;
    }
</style>
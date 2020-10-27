<template>
  <div>
    <Students v-bind:students="students" />
    <Subjects v-bind:subjects="subjects" />
  </div>
</template>

<script>
    import Students from "./layouts/Students.vue";
    import Subjects from "./layouts/Subjects.vue"
    import {StudentsInDb} from "../api/students"
    import {SubjectsInDb} from "../api/subjects"

    export default {
        components: {
            Students,
            Subjects,
        },
        data() {
           return {
                
            };
        },
        meteor: {
           students () {
             return StudentsInDb.find({}).fetch()
            },
           subjects () {
             return SubjectsInDb.find({}).fetch();
            },
        }
    };
</script>

<style>
</style>

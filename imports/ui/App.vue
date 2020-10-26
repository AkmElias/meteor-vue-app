<template>
  <div>
    <Students v-bind:students="students" />
  </div>
</template>

<script>
import Students from "./Students.vue";

export default {
  components: {
    Students,
  },
  data() {
    return {
      students: [
        {
          name: "Elias",
          email: "elias1@gmail.com",
          phone: 01879023909,
          DateOfBirth: "31 Dec 1994",
          Subject: "English",
        },
        {
          name: "Elias2",
          email: "elias1@gmail.com",
          phone: 01879023909,
          DateOfBirth: "31 Dec 1994",
          Subject: "English",
        },
        {
          name: "Elias3",
          email: "elias1@gmail.com",
          phone: 01879023909,
          DateOfBirth: "31 Dec 1994",
          Subject: "English",
        },
      ],
    };
  },
};
</script>

<style></style>

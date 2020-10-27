<template>
   <div>
    <h3>Add Student</h3>
    <div class='add-student'>
       <form @submit="addStudent">
         <input type="text" v-model="name" name="name" placeholder="name...">
         <input type="email" v-model="email" name="email" placeholder="email...">
         <input type="text" v-model="phone" name="phone" placeholder="phone...">
         <input type="date" v-model="dob" name="dob" placeholder="date of birth...">
         <button type='submit' class='btn'>ADD</button>
       </form>
    </div>
   </div> 
</template>
<script>
import uuid from 'uuid'
import {StudentsInDb} from '../../api/students'
export default {
    name: "AddStudent",
    data () {
          return {
              name: '',
              email: '',
              phone: '',
              dob: ''
            }
        },
    methods: {
       addStudent(e){
        e.preventDefault();
        const newStudent = {
                 _id: uuid.v4(),
                 name: this.name,
                 email: this.email,
                 phone: this.phone,
                 dateOfBirth: this.dob,
                 createdAt: new Date()
            }
         const res = StudentsInDb.insert(newStudent);
         console.log(res);
         this.name='',
         this.email='',
         this.phone='',
         this.dob=''
        },
    }
}
</script>

<style scoped>

</style>
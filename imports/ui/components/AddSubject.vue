<template>
  <div>
    <h3> Add Subject </h3>
    <div class='add-subject'>
        <form @submit="addSubject">
            <input type="text" v-model="name" name="name" placeholder="subject name...">
            <button type='submit' class='btn'>ADD</button>
        </form>
    </div>
  </div>
</template>

<script>
    import {SubjectsInDb} from '../../api/subjects';
    import uuid from 'uuid';
    export default {
        name: "AddSubject",
        data () {
            return {
                name: ''
            }
        },
        methods: {
           addSubject (e) {
               e.preventDefault()
               const newSubject = {
                   _id: uuid.v4(),
                   name: this.name,
                   createdAt: new Date()   
                }
                const res = SubjectsInDb.insert(newSubject)
                console.log(res)
                this.name = ''

            }
        }
    }

</script>

<style scoped>
</style>
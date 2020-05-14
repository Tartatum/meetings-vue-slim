<template>
  <div>
    <ol class="list-group">
      <li :key="person" v-for="person in list" class="list-group-item">
        {{ person.firstname }}
        {{ person.lastname }}
        <button  @click="deleteParticipant(person.id)" style="float: right; background-color:red; color:white" >Remove</button>
      </li>
    </ol>
  </div>
</template>

<script>
  export default {
    props: ['list'],
     methods: {
    deleteParticipant(id){
      this.$emit('deletePerson',id);
    }
  }
}
</script>

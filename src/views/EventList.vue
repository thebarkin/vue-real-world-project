<template>
  <div>
    <h1>Events List</h1>
    <EventCard v-for="event in events" :key="event.id" :event="event"/>
    <BaseIcon />
  </div>
</template>
<script>
import EventCard from "../components/EventCard";
import EventService from "@/services/EventService";
export default {
  components: {
    EventCard
  },
  data(){
    return {
      events:[]
    }
  },
  created(){
    EventService.getEvents().then(response=>{
      this.events = response.data;
    }).catch(err => {console.log(err)})
  }
}
</script>

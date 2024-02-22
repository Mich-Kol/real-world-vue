<script setup>
import EventCard from '@/components/EventCard.vue'
import { ref } from 'vue'

const events = ref([
  {
  id: 5928101,
  category: 'animal welfare',
  title: 'cat adoption day',
  description:'Find a feline',
  location:'Meow',
  date:'january 28, 2022',
  petsAllowed: true,
  organizer:'Kat',
},
{
id: 4582797,
  category: 'food',
  title: 'gardening',
  description:'plants',
  location:'flora city',
  date:'march 28, 2022',
  petsAllowed: true,
  organizer:'Fern',
},
{
  id: 7848541,
  category: 'sustainability',
  title: 'beach',
  description:'Trash',
  location:'Kokos',
  date:'july 28, 2022',
  petsAllowed: false,
  organizer:'Whale',
},
])

</script>

<template>
  <h1>Events for good</h1>
<div class="events">
  <EventCard v-for="event in events" :key="event.id" :event="event"/>
</div>
</template>
<style scoped>
.events {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
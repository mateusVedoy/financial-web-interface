<template>
    <div>
        <div @click="calendarToggle">
            <CalendarToogleComponent :showCalendar="this.showCalendar" @toggle-calendar="calendarToggle"/>
        </div>
        <div v-if="this.showCalendar">
            <Calendar :showCalendar="this.showCalendar" @toggle="calendarToggle"/>
        </div>
    </div>
</template>
<script>

import CalendarToogleComponent from '@/components/CalendarToogle.vue';
import Calendar from '@/components/Calendar.vue'

export default {
    name: "CalendarView",
    components: {
        CalendarToogleComponent,
        Calendar
    },
    data() {
        return {
            showCalendar: false
        }
    },
    methods: {
        calendarToggle() {
            this.showCalendar = !this.showCalendar;
        }
    }
}
</script>

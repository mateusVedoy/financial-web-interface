<template>
    <div class="toggle" v-if="!this.showCalendar">
        <div>
            <img src="../../public/img/schedule.png" alt="" />
        </div>
    </div>
</template>
<script>
export default {
    name: "CalendarToggleComponent",
    props: {
        showCalendar: {
            type: Boolean
        }
    }
}
</script>
<style scoped>
img {
    width: 3rem;
}

.toggle {
    background-color: #fff;
    border-radius: 1rem;
    width: 4rem;
    display: flex;
    align-items: center;
    justify-content: center;
    padding-top: 0.2rem;
    margin: 2rem 3rem;
}
</style>
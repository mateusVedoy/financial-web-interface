<template>
    <div class="calendar" v-if="this.showCalendar">
        <form action="">
            <h3>Choose a period</h3>
            <div>
                <label for="initialDate">Initial</label>
                <input type="date" name="initialDate" id="initialDate" placeholder="Initial">
            </div>
            <div>
                <label for="finalDate">Final</label>
                <input type="date" name="finalDate" id="finalDate">
            </div>
            <div class="bottom">
                <div class="btn-apply btn">
                    <h3>Apply</h3>
                </div>
                <div class="btn-cancel btn" @click="closeIt">
                    <h3>Cancel</h3>
                </div>
            </div>
        </form>
    </div>
</template>
<script>

export default {
    name: "CalendarComponent",
    props: {
        showCalendar: {
            type: Boolean
        }
    },
    methods: {
        closeIt() {
            this.$emit("toggle");
        }
    }
}

</script>
<style scoped>
.calendar {
    width: 10rem;
    background-color: #fff;
    border-radius: 1.6rem;
    padding: 1rem;
    margin: 1rem 1rem;
}

.calendar h3 {
    font-size: 1rem;
}

.calendar div {
    margin-top:1rem;
}

.bottom {
    gap: 1rem;
    font-size: .8rem;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 1rem;
}

.btn {
    border-radius: 1.6rem;
    width: 45%;
    align-items: center;
    justify-content: center;
    display: flex;
    cursor: pointer;
}

.btn-apply {
    background-color: #8694c7;
    color: #dfdfdf;
}

.btn-cancel {
    background-color: #e6e7ea;
    color: #8694c7;
}

form {
    font-size: 1rem;
    font-family: "Courier New", Courier, monospace;
    color: #898d93;
}

input[type="date"] {
    background-color: #8694c7;
    padding: .5rem;
    border-radius: .5rem;
    border: none;
    color: #fff
}
</style>
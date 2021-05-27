<template>
<div>
    <h1 class="text-7xl -my-6"> {{ time }}</h1>
    <h3 class="text-3xl -my-2"> {{ day }}</h3>
    <h3 class="text-3xl -my-2"> {{ month +  " " + date + ", " + year }}</h3>
</div>
</template>

<script>
export default {
  name: 'DateTime',
  data() {
    return {
      daysOfWeeK: ['SUNDAY', 'MONDAY', 'TUESDAY', 'WEDNESDAY', 'THURSDAY', 'FRIDAY', 'SATURDAY'],
      monthsInYear: ['JANUARY', 'FEBRUARY', 'MARCH', 'APRIL', 'MAY', 'JUNE', 'JULY', 'AUGUST', 'SEPTEMBER', 'OCTOBER', 'NOVEMBER', 'DECEMBER'],
      hours: '',
      minutes: '',
      seconds: '',
      day: '',
      date: '',
      month: '',
      year: '',
    };
  },
  computed: {
    time() {
      return `${this.hours}:${this.minutes}:${this.seconds}`;
    },
  },
  methods: {
    // TODO: Pad times
    createDate() {
      const date = new Date();
      this.hours = this.padTime(date.getHours());
      this.minutes = this.padTime(date.getMinutes());
      this.seconds = this.padTime(date.getSeconds());
      this.day = this.daysOfWeeK[date.getDay()];
      this.date = date.getDate();
      this.month = this.monthsInYear[date.getMonth()];
      this.year = date.getFullYear();
    },
    padTime(time) {
      if (time < 10) {
        return `0${time}`;
      }
      return time;
    },
  },
  mounted() {
    this.createDate();
    setInterval(() => { this.createDate(); }, 500);
  },
};
</script>

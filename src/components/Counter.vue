<template>
  <div>
    <div class="is-size-1">
      {{displayDays}} :
      {{displayHours}} :
      {{displayMinutes}} :
      {{displaySeconds}}

    </div>
  </div>
</template>

<script>
export default {
  name: 'Counter',
  data: () => ({
    displayDays: 0,
    displayHours:0,
    displayMinutes:0,
    displaySeconds:0
  }),
  computed: {
    _seconds: () => 1000,
    _minutes() {
      return this._seconds * 60
    },
    _hours() {
      return this._minutes * 60
    },
    _days() {
      return this._hours * 24
    }
  },
  mounted() {
    this.showRemaining()
  },
  methods: {
    showRemaining() {
      const timer = setInterval(() => {
        const now = new Date()
        const end = new Date(2021, 9, 6, 10, 10, 10, 10)
        console.log(end)
        const distance = end.getTime() - now.getTime()

        if (distance < 0) {
          clearInterval(timer)
          return
        }

        const days = Math.floor((distance/ this._days))
        const hours = Math.floor((distance % this._days) / this._hours)
        const minutes = Math.floor((distance % this._hours) / this._minutes)
        const seconds = Math.floor((distance % this._minutes) / this._seconds)
        this.displayMinutes = minutes < 10 ? '0' + minutes : minutes
        this.displaySeconds = seconds < 10 ? '0' + seconds : seconds
        this.displayHours = hours < 10 ? '0' + hours : hours
        this.displayDays = days < 10 ? '0' + days : days
      }, 1000)
    }
  }
}
</script>

<style scoped>
  
</style>
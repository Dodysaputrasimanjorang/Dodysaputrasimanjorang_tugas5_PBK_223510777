<template>
  <div class="text">
    © {{ companyName }} Since {{ yearText }}. 
  </div>
</template>

<script>
export default {
  name: 'Copyrights',
  data() {
    return {
      companyName: 'Simanjorang Diamond',
      startYear: 2024,
      currentYear: new Date().getFullYear()
    };
  },
  computed: {
    yearText() {
      return this.startYear === this.currentYear
        ? this.startYear.toString()
        : `${this.startYear} - ${this.currentYear}`;
    }
  }
};
</script>

<style scoped>
.text {
  font-family:'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  font-size: small;
}
</style>

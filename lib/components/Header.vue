<template>
  <div class="header">
    <div class="header-gocommons">
      <label class="title">
        <a href="https://go_commons.gitlab.io/home/" target="_blank">
          <span>GO!</span>Commons
        </a>
      </label>
    </div>
    <div class="header-project">
      <img class="project-logo" v-if="data.projectLogo" :src="$withBase(data.projectLogo)">
      <label for="title" class="title">{{ data.projectTitle }}</label>
    </div>
  </div>
</template>

<script>
export default {
  computed: {
    data() {
      return this.$page.frontmatter;
    }
  }
};
</script>

<style lang="stylus">
.header 
  display flex
  align-items center
  font-weight normal

.header-gocommons 
  margin-right 20px
  .title 
    font-size 1.8em  
    a 
      color black
      font-weight normal
      span
        color rgb(36, 163, 193)

.header-project 
  display flex
  align-items center
  .title
    font-size 1.5em
  .project-logo
    width 55px
    margin-right 10px

</style>


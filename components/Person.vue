<template>
  <div class="person">
    <div class="meta">
      <img :src="picture" :alt="name" class="picture">
      <a :href="mailTo" class="email">{{ email }}</a>
    </div>
    <div class="main">
      <div class="header">
        <h2 class="name">
          {{ name }}
        </h2>
        <a :href="linkedin" class="linkedin">
          <svg role="img" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><title>LinkedIn</title><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z" /></svg>
        </a>
      </div>
      <div class="description">
        {{ description }}
      </div>
      <div class="skills strongSkills">
        <h3>Strong Skills</h3>
        <ul>
          <li v-for="(skill, index) in strongSkills" :key="index">
            {{ skill }}
          </li>
        </ul>
      </div>
      <div class="skills aspiringSkills">
        <h3>Aspiring Skills</h3>
        <ul>
          <li v-for="(skill, index) in aspiringSkills" :key="index">
            {{ skill }}
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Card',
  props: {
    name: {
      type: String,
      required: true
    },
    linkedin: {
      type: String,
      required: true
    },
    email: {
      type: String,
      required: true
    },
    picture: {
      type: String,
      required: true
    },
    description: {
      type: String,
      required: true
    },
    strongSkills: {
      type: Array,
      required: true
    },
    aspiringSkills: {
      type: Array,
      required: true
    }
  },
  computed: {
    mailTo () {
      return `mailto:${this.email}`
    }
  }
}
</script>

<style lang="sass" scoped>
.person
  display: flex
  flex-direction: row
  flex-wrap: nowrap
  justify-content: flex-start
  align-content: stretch
  align-items: flex-start
  background: #ffffff // TODO css
  padding: 3rem
  gap: 4rem
  border-radius: 1rem // TODO css
  box-shadow: 0 0 1rem 0 rgb(0 0 0 / 6%) // TODO css
.meta
  display: flex
  flex-direction: column
  flex-wrap: nowrap
  justify-content: flex-start
  align-content: stretch
  align-items: stretch
  flex: 1 0 auto
  width: calc(100% / 3)
  .picture
    width: 100%
    margin: 0 0 2rem 0
    border-radius: 1rem // TODO css
  .email
    background: #ff2155 // TODO css
    border: 2px solid #ff2155 // TODO css
    color: #ffffff // TODO css
    padding: .75rem 2rem
    border-radius: 2rem // TODO css
    text-decoration: none
    transition: 120ms all ease-in-out // TODO css
    font-weight: bold
    overflow-wrap: break-word
    word-break: break-all
    text-align: center
    &:hover
      background: #ffffff // TODO css
      color: #ff2155 // TODO css
.main
  display: flex
  flex-direction: column
  flex-wrap: nowrap
  justify-content: flex-start
  align-content: stretch
  align-items: flex-start
  flex: 1 1 auto
  .header
    display: flex
    flex-direction: row
    flex-wrap: nowrap
    justify-content: flex-start
    align-content: stretch
    align-items: flex-start
    margin: 0 0 1rem 0
    .name
      font-weight: bold
      font-size: 2rem
      margin: 0 1rem 0 0
    .linkedin
      width: 2rem
      height: 2rem
      margin: 0.2rem 0 0 0
      svg
        fill: #0A66C2
        transition: 120ms all ease-in-out // TODO css
        &:hover
          transform: scale(1.1)
  .description
    margin: 0 0 2rem 0
  .skills
    h3
      font-weight: bold
      font-size: 1.2rem
      margin: 0 0 .25rem 0
    ul
      display: flex
      flex-direction: row
      flex-wrap: wrap
      justify-content: flex-start
      align-content: flex-start
      align-items: flex-start
      li
        background: #f8f8f8 // TODO css
        border-radius: 2rem // TODO css
        padding: .75rem 2rem
        margin: 0 1rem 1rem 0
  .strongSkills
    margin: 0 0 1rem 0
</style>

<template>
  <section>
    <ul>
      <li v-for="(person, index) in mock" :key="index">
        <Person v-bind="person" />
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  data () {
    return {
      mock: [
        {
          name: 'Paco Puylaert',
          linkedin: 'https://www.linkedin.com/in/paco-puylaert-b720308b/',
          email: 'paco.puy.pp@gmail.com',
          picture: 'https://uploads-ssl.webflow.com/61360796ce20579fa4e94dc3/613618cf6048e483a4b3b344_Paco%20Puylaert.png',
          description: 'I am a Product Designer passionate about impactful and valuable experiences. with a background in UX and Brand design, I worked with several companies with the goal to elevate their Products and Branding. Portfolio at - https://www.puylaertpaco.com/',
          strongSkills: ['Product Design (UX/UI)', 'Brand Design', 'User testing', 'Web development', 'Tech & Business'],
          aspiringSkills: ['Sales', 'Finance', 'Public speaking']
        },
        {
          name: 'Per K. Jensen',
          linkedin: 'https://www.linkedin.com/in/perkjensen/',
          email: 's113060@dtu.dk',
          picture: 'https://uploads-ssl.webflow.com/61360796ce20579fa4e94dc3/6136207cf504ac624456532f_Per%20K.%20Jensen.png',
          description: 'I am a technically well-founded mechanical engineer with a problem-solving mindset! I thrive working in a team full of diversity driven by passion and skills My main focus is hard-tech start ups within sustainable solutions. Hit me up and let us work together! 💪',
          strongSkills: ['Mechanical understanding', 'Interdiscipli- nary work', 'Solution finder', 'Tecnology assessment', 'Team dynamics'],
          aspiringSkills: ['Business design', 'Sustainable assessments', 'Funding']
        }
        // {
        //   name: '',
        //   linkedin: '',
        //   email: '',
        //   picture: '',
        //   description: '',
        //   strongSkills: ['', ''],
        //   aspiringSkills: ['', '']
        // }
      ]
    }
  }
}
</script>

<style lang="sass" scoped>
ul
  li
    margin: 0 0 4rem 0
</style>

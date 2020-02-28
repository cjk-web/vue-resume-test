<template>
  <div id="app">
    <Resume v-bind:person="me" />
    <Skills v-bind:skills="me.quickSkills" />
  </div>
</template>

<script>
import Skills from './components/Skills';
import Resume from './components/Resume';

export default {
  name: 'App',
  components: {
    Skills,
    Resume
  },
  data() {
    return {
      me: {
        name: {
          first: "Caleb",
          last: "Kosinski"
        },
        job: "Web Developer",
        profile: "Proficient web developer with 5+ years of experience. Adept at designing and building responsive, mobile friendly websites. Collaborated on several website redesigns resulting in increased sales and improved search rankings. Experienced in .NET development, including ASP and MVC, and JavaScript development using both React and Angular frameworks.",
        experience: [
          {
            id: 1,
            company: "PageBean LLC",
            position: "Web Developer",
            duration: {
              start: "2015",
              end: "2018"
            },
            responsibilities: [
              {
                id: 1,
                details: "Collaborated on building and redesigning e-commerce websites with a focus on responsive design and improving user experience. Communicated with customers on design options and suggestions."
              },
              {
                id: 2,
                details: "Handled front end development to maintain and update existing websites."
              },
              {
                id: 3,
                details: "Implemented and improved ADA compatibility based on WCAG 2.0 standards."
              },
              {
                id: 4,
                details: "Developed solutions for cross browser compatibility issues."
              }
            ] 
          },
          {
            id: 2,
            company: "Self Employed",
            position: "Web Developer",
            duration: {
              start: "2018",
              end: "Present"
            },
            responsibilities: [
              {
                details: "Worked on designing and building front-end/UI for various web based projects."
              },
              {
                details: "Built UI for both React and Phoenix based customer management systems."
              },
            ] 
          }
        ],
        skills: [
          {
            id: 1,
            details: "Strong skills in HTML, CSS (including Sass/SCSS preprocessors), JavaScript, and JQuery"
          },
          {
            id: 2,
            details: "Experience in both Team Foundation Server and Git version control systems."
          },
          {
            id: 3,
            details: "Knowledge of multiple frameworks including React, Angular, Phoenix, Elixir, and Bootstrap."
          },
          {
            id: 4,
            details: "Familiar with using Adobe software for development including Illustrator, Photoshop, XD, and more."
          }
        ],
        quickSkills: [
          {
            id: 1,
            category: "Languages",
            skills: [
              {
                id: 1,
                title: "HTML"
              },
              {
                id: 2,
                title: "CSS"
              },
              {
                id: 3,
                title: "Sass"
              },
              {
                id: 4,
                title: "SCSS"
              },
              {
                id: 5,
                title: "c#"
              },
              {
                id: 6,
                title: "JavaScript"
              },
              {
                id: 7,
                title: "jQuery"
              },
            ]
          },
          {
            id: 2,
            category: "Version Control",
            skills: [
              {
                id: 1,
                title: "Git"
              },
              {
                id: 2,
                title: "TFS"
              },
              {
                id: 3,
                title: "SVN"
              },
            ]
          },
          {
            id: 3,
            category: "Frameworks",
            skills: [
              {
                id: 1,
                title: "Angular"
              },
              {
                id: 2,
                title: "React"
              },
              {
                id: 3,
                title: "Vue.JS"
              },
              {
                id: 4,
                title: "Bootstrap"
              },
              {
                id: 5,
                title: "Phoenix"
              },
              {
                id: 6,
                title: "Elixir"
              },
            ]
          }
        ]
      }
    }
  }
}
</script>

<style lang="sass">
*
  margin: 0
  padding : 0
#app
  font-family: Avenir, Helvetica, Arial, sans-serif
  display: flex
  min-height: 100vh
  height: 100%
</style>

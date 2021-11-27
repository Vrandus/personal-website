<template>
  <section class="section">
    <About title="About Me" id="about">
      Raised in the suburbs of Toronto, I'm a York University graduate 
      currently working in the finance space as a Software Engineer.
    </About>
    <h1 class="project" id="work-experience">
      Work Experience
    </h1>
    <Work
    v-for="experience in experiences"
    :key="experience.employer"
    :employer="experience"
    />
    <h1 class="project">Projects</h1>
    <div class="columns is-desktop" id="projects">
      <card title="ChatCraft" icon="discord" link="https://github.com/Vrandus/Chatcraft">
        My friends and I wanted to play some Minecraft, but it was hard to keep track of what went on in game and seeing who was online. So I created a Discord bot that can be integrated into a Discord text channel that would relay the in-game chat to the channel and vice versa.
      </card>

      <card title="Number Recognizing MLP" icon="layers" link="https://github.com/Vrandus/Number-Recognition-MLP">
        A multilayer perceptron trained on a subset of the MNIST data set. I created it with the help of old school notes. 
        It currently runs at an accuracy rate of 97.7% using a certain number of hidden nodes. Created with Golang, there is also functionality to 
        run the neural network on a 28x28 png.
      </card>

      <card title="DCIM Importer" icon="folder-outline" link="https://github.com/Vrandus/DCIM-Importer">
        The worst part of photography is having to import and organize your images. I had a back-log of 10k+ images on a number of SD cards, 
        so I made a command-line program to efficiently copy files into an organized file structure. I also learned Golang along the way.


      </card>
    </div>
    <h1 class="project" id="hobbies">Hobbies</h1>

  </section>
</template>

<script>
import Card from '~/components/Card'
import Hero from '~/components/Hero'
import About from  '~/components/About'
import Work from '~/components/Work'
export default {
  name: 'HomePage',

  components: {
    Card,
    Hero
  },
  data() {
    return{
      experiences : [
                {
          employer : "Citibank",
          title: "Software Development Analyst",
          logo : "/Citi.png",
          dates : "July 2021 - Present",
          content : "At Citibank, I was able to work on data intensive applications and was given the chance to lead multiple projects soon after starting. I was put on a trading and business analytics project in our CitiVelocity application to visualize various factors, such as expense, profit, revenue, across the entirety of Citi. In this project, we needed to filter certain data based on a user's permissions. So, I led a project to develop a permissions microservice which would interface with our tableau dashboards and update views/licensing based on the user's permissions in CitiVelocity. After successfully deploying and delivering the dashboard and services, we gained more attention from directors and above, which signalled to us that we needed to increase the scope of our existing microservices to be generic and handle the any number of future dashboards.",
          isFlipped: false
        },
        {
          employer : "AMD",
          title: "Software Development Engineer Intern",
          logo : "/amd-red.png",
          dates : "October 2020 - June 2021",
          content: "At AMD, I was assigned a full-stack project to be the lead developer on. I was to develop and maintain an existing web application that would queue up and send tasks to remote machines running MacOS. I got to learn Vue.js (made this website with it) to develop the frontend and used node for the backend. I also worked on a remote client that would wait to receive a list of tests, which would run and insert the results onto a database. I was also tasked with migrating the entire codebase, the web app and the remote client, to AMD’s internal GIT for proper version control. I implemented agile methodology by creating and organizing JIRA tickets on a Kanban board for features and bugs to help with morning stand-ups.",
          isFlipped: true
        },
        {
          employer : "Jupio Labs",
          title: "Software Engineer Intern",
          logo : "/jupio.png",
          dates : "September 2018 - January 2019",
          content : "Jupio Labs is a small web development firm based in Toronto that specialized in creating web applications for political candidates and local businesses. I learned a lot about how modern and responsive web development is done using React and Node.js. I was also taught the benefits of creating reusable react components as I was later able to repurpose them for other projects with some minor changes.",
          isFlipped: false
        },

      ]
    }
  }
}
</script>

<style>
  #about {
    font-size: 1.2rem;
  }
  .work {
    margin: 1rem auto;
    text-align: center;
  }
  .project{
    margin: 2rem auto;
    margin-top: 3rem;
    text-align: center;
  }
</style>
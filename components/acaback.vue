<template>
  <div class="acaback">
    <p class="headline">Project</p>
    <p></p>
    <div class="list">
      <img
        :src="require(`@/assets/img/projects/${projects[index - 1].image}`)"
        :alt="projects[index - 1].alt"
        class="project grayEffect"
      />
      <img
        :src="require(`@/assets/img/projects/${projects[index].image}`)"
        :alt="projects[index].alt"
        class="project mainProject"
      />
      <img
        :src="require(`@/assets/img/projects/${projects[index + 1].image}`)"
        :alt="projects[index + 1].alt"
        class="project grayEffect"
        @click.prevent="goLeft"
      />
    </div>
    <div class="content">
      <p class="title">{{ projects[index].title }}</p>
      <p class="decription">{{projects[index].dexcription }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          title: "Snek",
          dexcription: "Description du parcours dans cette école.  Lorem ipsum dolor sit amet et Rabat Lorem ipsum dolor sit amet et Lorem ipsum dolor sit amet et Lorem ipsum dolor sit amet et",
          source: "https://github.com/abdellakh/Snek",
          image: "Snek_Project.jpg",
          alt: "Snek Project",
        },
        {
          title: "Ruche Connectées",
          dexcription:
            "Description du parcours dans cette école.  Lorem ipsum dolor sit amet et Rabat Lorem ipsum dolor sit amet et Lorem ipsum dolor sit amet et Lorem ipsum dolor sit amet et",
          source: "https://gitlab.com/p6719/projet-tech",
          image: "Ruche_Project.jpg",
          alt: "Ruche Connectées Project",
        },
        {
          title: "My Strong Kid",
          dexcription: "Description du parcours dans cette école.  Lorem ipsum dolor sit amet et Rabat Lorem ipsum dolor sit amet et Lorem ipsum dolor sit amet et Lorem ipsum dolor sit amet et",
          source: "https://github.com/anasidsaleh/my-strong-kid-app",
          image: "My_Strong_kid_mini.jpg",
          alt: "My Strong Kid Project",
        },
        {
          title: "Ruche Connectées",
          dexcription:
            "Description du parcours dans cette école.  Lorem ipsum dolor sit amet et Rabat Lorem ipsum dolor sit amet et Lorem ipsum dolor sit amet et Lorem ipsum dolor sit amet et",
          source: "https://gitlab.com/p6719/projet-tech",
          image: "Ruche_Project.jpg",
          alt: "Ruche Connectées Project",
        },
      ],
      index: 1
    };
  },
  methods: {
    goRight() {
    },
    goLeft() {
      this.index = this.index + 1 > this.projects.length ? this.projects.length -1 : this.index + 1 
      console.log(this.index)
    },
  },
};
</script>

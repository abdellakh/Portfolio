<template>
  <div class="main">
    <div class="sticky_bar">
      <div class="logo">
        <img src="../assets/img/Logo_test.png" alt="" class="mainLogo" />
      </div>
      <div @click="blabla()" class="menu">
        <div v-for="(item, index) in items" :key="index" class="element">

          <div :class="{titles : !item.isButton, contact: item.isButton}" @click.stop="goTo(item.href)">
            {{ item.title }}
          </div>


          <!-- <p v-if="item.title != 'Contact'" href="" class="titles">
            {{ item.title }}
          </p>
          <button v-else @click="openPop" class="contact">
            <p class="titles">{{ item.title }}</p>
          </button> -->
        </div>
      </div>
    </div>
    <div class="home">
      <div class="welcome">
        <div>
          <p >Hi ! I am</p>
          <p class="myName">Abdellah Khouya</p>
          <p >
            I am a {{role}}developer
          </p>
        </div>
      </div>
      <div class="myProfile">
        <img src="../assets/img/Logo_test.png" alt="" class="profil" />
      </div>
    </div>
    <acaback/>
    <div class="test">
      <div class="testdetest2"></div>
      <div class="testdetest"></div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { title: "Acceuil", href: "home" },
        { title: "Mon Parcours", href: "acaback" },
        { title: "Projets", href: "projects" },
        { title: "Compétences", href: "skills" },
        { title: "Contact", href: "footer", isButton: true },
      ],
      role: ""
    };
  },
  methods: {
    changeRole() {
      // setInterval to change role every 10 seconds
    }
  }
};
</script>

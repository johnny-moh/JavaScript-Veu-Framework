<script >
const pics = ['../public/images/image1.jpeg', '../public/images/image2.jpeg', '../public/images/image3.jpeg',
  '../public/images/image4.jpeg', '../public/images/image5.jpeg', '../public/images/image6.jpg']

export default {

  data() {
    return {
      message: 'Hello Vue!',

      pics,
      picturesImage: pics[4],
    }
  },




  methods: {

    updateImage(id) {
      console.log(this.picturesImage);
      this.picturesImage = this.pics[id]
    },
    resetImage() {
      this.picturesImage = pics[2]
    }




  }

}


</script>





<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />
  </header>

  <main>
    <img :src="picturesImage" @mouseover="updateImage(5)" @mouseleave="resetImage" />
    
  </main>

</template>





 <style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style> 

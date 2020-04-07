<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" /> -->
    <figure>
      <img
        @click="clickMethod"
        src="https://sevensidedmarble.com/images/org-mode.png"
        alt="Org mode is great for writing structured content like scripts."
        :class="imageProperty"
      />
      <figcaption>
        Org mode is great for writing structured content like scripts.
      </figcaption>
    </figure>

    <p>
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nesciunt
      laudantium labore deserunt repellat, impedit et id non optio hic officiis
      aperiam ipsam inventore repudiandae aliquam eius aliquid exercitationem
      sint illum.
    </p>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nesciunt
      laudantium labore deserunt repellat, impedit et id non optio hic officiis
      aperiam ipsam inventore repudiandae aliquam eius aliquid exercitationem
      sint illum.
    </p>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nesciunt
      laudantium labore deserunt repellat, impedit et id non optio hic officiis
      aperiam ipsam inventore repudiandae aliquam eius aliquid exercitationem
      sint illum.
    </p>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "Home",
  components: {
    // HelloWorld,
  },
  computed: {},
  data() {
    return {
      imageProperty: "normal",
      clicked: true,
    };
  },
  methods: {
    clickMethod() {
      console.log(this.clicked);
      this.clicked = !this.clicked;
      // this.imageProperty = "clicked";
      if (this.clicked) {
        this.imageProperty = "expand";
      } else {
        this.imageProperty = "normal";
      }
    },
  },
  // watch: {
  //   click_status(clicked) {
  //     if (clicked) {
  //       this.imageProperty = "expand";
  //     }
  //   },
  // },
};
</script>

<style scoped>
.normal {
  width: 500px;
  transition: all 0.5s ease;
}

.expand {
  width: 1000px;
  transition: all 0.5s ease;
}
</style>

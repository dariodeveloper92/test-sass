<template>
  <header>
    <a href="/">
    <img src="@/assets/img_deadpool.jpg" alt="">
    </a>
  

  <nav>
      <ul>
          <li v-for="(link, index) in links" :key="index"> 
              <a :class="(link.current)" href="link.url">
                  {{ link.text }}
              </a>
          </li>
          <li><a href="#"> Home</a></li>
          <li><a href="#"> Chi siamo</a></li>
          <li><a href="#"> prodotti</a></li>
          <li><a href="#"> Contatti</a></li>
      </ul>
  </nav>
</header>
</template>

<script>
export default {
  name: 'Header',
  
  data() {
      return {
          links: [
              {
                  text: "Home",
                  url: "#",
                  current: false,
              },
              {
                  text: "Prodotti",
                  url: "#",
                  current: true,
              },
              {
                  text: "Chi siamo",
                  url: "#",
                  current: false,
              },
              {
                  text: "Contatti",
                  url: "#",
                  current: false,
              },
          ]
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    @import "../style/mixins";
    @import "../style/vars";

    header {
        text-align: center;

        ul {
            list-style: none;
            @include center();

            li a {
                display: inline-block;
                padding: 1rem;
                text-decoration: none;
                font-weight: 600;
                transition: color 0.3s;

                &:hover,
                &:active {
                    color: red;
                }
            }
        }
    }
</style>

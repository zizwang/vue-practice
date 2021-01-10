<template>
  <div class="home">
    <div class="item1"><Header/></div>
    <div class="item2"><List/></div>
    <div class="item3"><MainContent msg="MainContent"/></div>
    <div class="item4"><Footer /></div>
  </div>
</template>

<script>
// @ is an alias to /src
import MainContent from '@/components/MainContent.vue'
import Header from '@/components/Header.vue'
import List from '@/components/List.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: 'Home',
  components: {
    MainContent,
    Header,
    List,
    Footer
  }
}
</script>

<style scoped>
.item1 {
  grid-area: header;
}

.item2 {
  grid-area: list;
}

.item3 {
  grid-area: main;
}

.item4 {
  grid-area: footer;
}

.home {
  display: grid;
  grid-template-areas:
    'header header header header'
    'list main main main'
    'footer footer footer footer';
  grid-gap: 10px;
}

.home > div {
  text-align: center;
  border: 1px solid black;
}
</style>
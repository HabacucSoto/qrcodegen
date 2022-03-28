<template>
  <nav class="d-flex justify-content-between align-items-center">
    <div id="logo">
      <h1>qrcodegen</h1>
    </div>
    <div id="icons" class="d-flex justify-content-between towidth align-items-center">
      <a href="https://github.com/HabacucSoto" target="_blank">
        <i class="bi bi-github navicon"></i>
      </a>
      <a href="https://www.linkedin.com/in/habacucsoto/" target="_blank">
        <i class="bi bi-linkedin navicon"></i>
      </a>
      <a href="https://www.instagram.com/habacuc.soto/" target="_blank">
        <i class="bi bi-instagram navicon"></i>
      </a>
    </div>
  </nav>
  <Content />
</template>

<script>
import Content from '@/components/Content'
export default {
  components: {
    Content
  }
}
</script>

<style scoped>
  nav {
    width: 100%;
    height: 80px;
  }
  h1 {
    font-family: 'Exo', sans-serif;
    font-weight: 800;
  }
  i {
    font-size: 2.5vw;
    color: #fff;
  }
  .towidth {
    width: 25%;
  }
  #logo {
    margin-left: 5%;
  }
  #icons {
    margin-right: 5%;
  }

  @media (max-width: 800px) {
    i {
      font-size: 5vw;
    }
  }
  @media (max-width: 700px){
    i {
        color: #4863E6;
    }
    nav {
      border-bottom: 1.5px solid #ccc;
    }
  }
</style>

<template>
  <section :class="st">
    <div class="container">
      <div class="row">
        <div class="col-lg-12">
          <nav class="navbar navbar-expand-lg">
            <a class="navbar-brand" href="index.html">
              <img src="../assets/images/white-logo.svg" alt="Logo" />
            </a>
            <button
                @click="btn_activate" :aria-expanded="{'true': btn_st===0, 'false': btn_st===1}"
                :class="{'navbar-toggler': true, 'active': btn_st===0, 'collapsed':btn_st===1}"
                type="button" data-bs-toggle="collapse" data-bs-target="#navbarNine"
                aria-controls="navbarNine" aria-label="Toggle navigation">
              <span class="toggler-icon"></span>
              <span class="toggler-icon"></span>
              <span class="toggler-icon"></span>
            </button>

            <div :class="{'collapse navbar-collapse sub-menu-bar': true, 'show': btn_st===0}" id="navbarNine">
              <ul class="navbar-nav me-auto">
                <li class="nav-item">
                  <a class="page-scroll active" href="#hero-area">Top</a>
                </li>
                <li class="nav-item">
                  <a class="page-scroll" href="#services">link 1</a>
                </li>

                <li class="nav-item">
                  <a class="page-scroll" href="#pricing">link 2</a>
                </li>
                <li class="nav-item">
                  <a class="page-scroll" href="#contact">link 3</a>
                </li>
              </ul>
            </div>

            <div @click="sidebar_activate" class="navbar-btn d-none d-lg-inline-block">
              <a class="menu-bar" href="#side-menu-left"><i class="lni lni-menu"></i></a>
            </div>
          </nav>
          <!-- navbar -->
        </div>
      </div>
      <!-- row -->
    </div>
    <!-- container -->
  </section>
</template>

<script>
export default {
  name: "NavBar",
  data (){
    return{
      st: 'navbar-area navbar-nine sticky',
      btn_st: 1
    }
  },
  methods:{
    sticky(){
      this.st = 'navbar-area navbar-nine sticky';
    },
    sidebar_activate(){
      this.$emit('create');
    },
    btn_activate(){
      this.btn_st === 0 ? this.btn_st = 1: this.btn_st = 0;
    }
  }
}
</script>

<style scoped>

</style>
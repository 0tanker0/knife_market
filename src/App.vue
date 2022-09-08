<template>
  <nav-bar
    @create= "sidebar_activate">
  </nav-bar>

  <side-bar
    :sidebar_st="sidebar_st"
    @remove="sidebar_deactivate">
  </side-bar>

  <slider></slider>
  <header-area></header-area>
  <photo-block></photo-block>
  <about-five-part></about-five-part>
  <cta-area></cta-area>
  <latest-news-area></latest-news-area>
  <brand-area></brand-area>
  <contact-section></contact-section>
  <map-section></map-section>
  <footer-area></footer-area>

  <a href="#" class="scroll-top btn-hover">
    <i class="lni lni-chevron-up"></i>
  </a>

</template>

<script>

import NavBar from "@/components/NavBar";
import SideBar from "@/components/SideBar";
import AboutFivePart from "@/components/AboutFivePart";
import CtaArea from "@/components/CtaArea";
import LatestNewsArea from "@/components/LatestNewsArea";
import BrandArea from "@/components/BrandArea";
import ContactSection from "@/components/ContactSection";
import MapSection from "@/components/MapSection";
import FooterArea from "@/components/FooterArea";
import HeaderArea from "@/components/HeaderArea";
import Slider from "@/components/Slider";
import PhotoBlock from "@/components/PhotoBlock";
export default {
  name: 'App',
  components: {
    PhotoBlock,
    Slider,
    HeaderArea,
    FooterArea,
    MapSection, ContactSection, BrandArea, LatestNewsArea, CtaArea, AboutFivePart, SideBar, NavBar},
  data () {
    return {
      sidebar_st: 1
    }
  },
  methods:{
    sidebar_activate(){
      if (this.sidebar_st === 1){
        this.sidebar_st = 0;
        console.log('Opening sidebar');
      } else {
        this.sidebar_st = 1;
        console.log('Closing sidebar');
      }
    },
    sidebar_deactivate(){
      this.sidebar_st = 1;
    }
  }
}
</script>

<style>
</style>

<template>
  <div style="background-color: #F4F1EA; ">

    <div style="margin-bottom: 9rem;">
      <Navbar/>
      <Cover/>
      <Belief/>
      <div style="background-color: #F7F6F4;">
        <Monastery/>
      </div>
      <div style="background-color: #C9A081;">
        <Sacred/>
      </div>
      <div style="background-color: #F4F1EA;">
        <Fortune/>
      </div>
    </div>
    <Footer/>
  </div>
</template>

<script>

import Navbar from '../components/nav/navbar';
import Cover from "~/components/cover/cover";
import Belief from "~/components/belief/belief";
import Monastery from "~/components/monastery/monastery";
import Sacred from "~/components/sacred/sacred";
import Fortune from "~/components/fortune/fortune";
import Footer from "~/components/footer/footer";

export default {
  name: "index",
  components: {
    Footer,
    Fortune,
    Sacred,
    Monastery,
    Belief,
    Cover,
    Navbar,
  }
};

</script>

<style>

</style>

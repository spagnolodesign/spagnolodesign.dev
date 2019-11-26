<template>
  <div>
    <h2 id="title" class="title bring-up">
      <span>B</span><span>u</span><span>o</span><span>n</span><span>a</span><span>s</span><span>e</span><span>r</span><span>a</span>
    </h2>
    <h2 id="title-two" class="title title-black">
      <span>S</span><span>i</span><span>m</span><span>p</span><span>l</span><span>i</span><span>c</span><span>i</span><span>t</span><span>y</span>
    </h2>
  </div>
</template>

<script>

import gsap from 'gsap';

export default {
  props: ['text'],
  mounted() { 
    const title = this.$refs.title;
    const easing = "slow(0.7, 0.5, false)";

    var tl = gsap.timeline();
    tl.from('#title span', {
      y: "+=10",
      x: "+=15",
      duration: .30,
      opacity: 0,
      rotation: 10,
      stagger: {
        amount: 1,
        from: "right"
      },
      ease: easing
    });
    
    tl.from('#title-two span', {
      y: "+=25",
      x: "+=15",
      duration: .20,
      opacity: 0,
      rotation: 7,
      stagger: {
        amount: 1,
        from: "right"
      },
      ease: easing
    });
    // console.log(title)
  }
}
</script>

<style>

.title span{
  display: inline-block;
}

</style>
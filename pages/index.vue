<template>
  <div class="container">
    <section class="container__content">
    <div class="container__hero" data-lax-translate-y="0 0, 100 -200">
      <h1 data-lax-opacity="0 1, 470 0">Lorem, ipsum.</h1>
      <span data-lax-opacity="0 1, 100 0">scroll down</span>
    </div>
    <div class="container__main" data-lax-translate-y="0 600, 100 -500">
      <h2>Lorem, ipsum dolor.</h2>
      <h3>Lorem ipsum dolor sit amet.</h3>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Veniam facilis maxime ducimus vero voluptatibus cum at aspernatur natus hic alias libero accusamus minima voluptates animi quas, nihil dignissimos, blanditiis laborum aut quod pariatur quisquam adipisci! Cupiditate maxime quia exercitationem, ad aspernatur nam minima eum omnis modi ullam a odio libero itaque dolorum magnam autem hic atque repellat accusantium. Nostrum magni ratione ad perspiciatis provident nisi fugit officiis rerum voluptates amet? Itaque aut facilis facere repellat nobis earum cupiditate voluptates iusto blanditiis beatae, sint exercitationem, dicta, culpa eius debitis eaque? Velit laboriosam excepturi reprehenderit sunt illo vel voluptas quisquam consequuntur fugit!</p>
    </div>
    </section>
    <div class="asset5" data-lax-translate-x="0 0, 500 -500"></div>
    <div class="asset8" data-lax-translate-x="0 0, 800 300" data-lax-opacity="0 .7, 470 0"></div>
    <div class="asset6" data-lax-translate-x="0 0, 700 200" data-lax-translate-y="0 0, 800 -200 | speed=2"></div>
    <Asset9 data-lax-translate-x="0 -400, 400 -100" data-lax-opacity="0 .7, 470 0"/>
    <div class="asset7" data-lax-translate-x="0 0, 600 -300 | speed=2"></div>
  </div>
</template>

<script>
if(process.client) {
  var lax = require("lax.js");
}
import Asset9 from "~/components/Asset9";
export default {
  components:{
    Asset9,
  },
  methods:{
    loaded() {
      lax.setup();
      document.addEventListener('scroll', function(x){
      lax.update(window.scrollY)
      }, false) 
    }
  }, 

  mounted(){
    this.loaded();
    lax.addElement(this.$el.querySelector('.asset9'),)
    lax.addElement(this.$el.querySelector('.asset7'))
    lax.addElement(this.$el.querySelector('.asset6'))
    lax.addElement(this.$el.querySelector('.asset8'))
    lax.addElement(this.$el.querySelector('.asset5'))
    lax.addElement(this.$el.querySelector('.container__hero h1'))
    lax.addElement(this.$el.querySelector('.container__hero span'))
    lax.addElement(this.$el.querySelector('.container__hero'))
    lax.addElement(this.$el.querySelector('.container__main'))
  }
}
</script>

<template>
  <!-- HERO-HEADER -->
  <section class="hero-header" id="hero-header">
    <no-sar>
       <div class="hero-wrap">
        <!-- 左 -->
        <div class="hero-title-catch hero-title-position">
           <div ref="ref_1" class="hero-title ff_Athelas sample-text">走りをスマートに</div>
           <div ref="ref_3"  class="hero-sub-title ff_Avenir_Next_Condensed sub1 sample-text2">BE SMART SPRINT</div>
        </div>
        <!-- 右 -->
          <div class="hero-title-name hero-title-position">
             <div ref="ref_2" class="hero-title ff_Avenir_Next sample-text1">SMARTDASH</div>
             <div ref="ref_4" class="hero-sub-title ff_Avenir_Next_Condensed sub2
             sample-text3">SCIENCE×SPORTS</div>
          </div>
          <video class="mov" src="~/assets/movies/top-movie2.mp4" autoplay muted playsinline loop>
               <p>動画を再生するにはvideoタグをサポートしたブラウザが必要です。</p>
          </video>
       </div>
    </no-sar>
  </section>
</template>

<style>
.NuxtLogo {
  animation: 1s appear;
  margin: auto;
}

@keyframes appear {
  0% {
    opacity: 0;
  }
}
</style>

<script>
export default {
    mounted() {
        const elem1 = this.$refs.ref_1;
        const elem2 = this.$refs.ref_2;
        const elem3 = this.$refs.ref_3;
        const elem4 = this.$refs.ref_4;
        
        setTimeout(function(){
          elem1.classList.add('show');
          elem2.classList.add('show');
          elem3.classList.add('show');
          elem4.classList.add('show');
        }, 2200);
    }
}
</script>
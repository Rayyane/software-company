<template>
    <!-- Hero Section -->
    <section id="hero" class="hero section dark-background">
      <div class="container" data-aos="fade-up">
        <div class="row align-items-center">
          <div class="col-lg-6">
            <div class="hero-content" data-aos="fade-up" data-aos-delay="100">
              <div class="hero-tag">
                <i class="bi bi-rocket-takeoff"></i>
                <span>Innovative Solutions</span>
              </div>
              <Transition name="fade-in">
                <div v-if="show">
                  <h1>Achieving <span class="highlight">Outstanding Results</span> for Your Growth</h1>
                  <p class="lead">Our dedicated team provides exceptional service to help you reach your business goals effectively.</p>
                  <ul class="hero-features">
                    <li><i class="bi bi-check-circle"></i> Streamlined operational processes</li>
                    <li><i class="bi bi-check-circle"></i> Enhanced customer engagement strategies</li>
                    <li><i class="bi bi-check-circle"></i> Data-driven decision support</li>
                  </ul>
                  <div class="hero-cta">
                    <a href="#services" class="btn btn-primary">Explore Our Services</a>
                    <a href="tel:+1 (555) 987-6543" class="btn btn-link"><i class="bi bi-telephone"></i> +1 (555) 987-6543</a>
                  </div>
                </div>
              </Transition>
            </div>
          </div>
          <div class="col-lg-6">
            <!-- <Transition name="fade-in">
              <div v-if="show" class="hero-image" data-aos="fade-up" data-aos-delay="200">
                <img src="../assets/img/hero/hero-image.webp" alt="Hero Image" class="img-fluid">
              </div>
            </Transition> -->
            <Transition name="fade-in-right">
              <div v-if="show" class="hero-image-wrapper">
                <img src="../assets/img/about/about-square-13.webp" alt="" class="img-fluid hero-image">
                <div class="stat-card top-right">
                  <div class="stat-value">18.9K</div>
                  <div class="stat-label">Improved market presence</div>
                  <div class="stat-icon">
                    <i class="bi bi-graph-up-arrow"></i>
                  </div>
                </div>
                <div class="stat-card bottom-left">
                  <div class="stat-value">+450%</div>
                  <div class="stat-label">Increased lead generation</div>
                  <div class="stat-icon">
                    <i class="bi bi-graph-up"></i>
                  </div>
                </div>
              </div>
            </Transition>
          </div>
        </div>
      </div>
    </section><!-- /Hero Section -->
</template>

<script setup>
import { onMounted, ref } from 'vue'; 

const show = ref(false);

onMounted(() => {
  setTimeout(() => {
    show.value = true;
  }); // Delay to simulate loading
});
</script>

<style scoped>
.fade-in-enter-active {
  transition: all 1s ease;
}
.fade-in-enter-from {
  transform: translateX(-100px);
  opacity: 0;
}
.fade-in-enter-to {
  transform: translateX(0);
  opacity: 1;
}

.fade-in-right-enter-active {
  transition: all 1s ease;
}
.fade-in-right-enter-from {
  transform: translateX(100px);
  opacity: 0;
}
.fade-in-right-enter-to {
  transform: translateX(0);
  opacity: 1;
}
</style>
<!-- TeamSection.vue -->
<template>
  <section id="team" class="team section">
    <div class="container section-title" data-aos="fade-up">
      <h2>Team</h2>
      <p>Necessitatibus eius consequatur ex aliquid fuga eum quidem sint consectetur velit</p>
    </div>

    <div class="container" data-aos="fade-up" data-aos-delay="100">
      <div class="row">
        <!-- Intro Column -->
        <div class="col-lg-4 team-intro" data-aos="fade-right" data-aos-delay="200">
          <div class="team-intro-content">
            <h2>Meet Our Experts</h2>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin vestibulum dui sed justo finibus, in gravida felis iaculis.
              Suspendisse potenti.
            </p>
            <div class="team-navigation">
              <button ref="prevEl" class="team-nav-prev">
                <i class="bi bi-arrow-left"></i>
              </button>
              <button ref="nextEl" class="team-nav-next">
                <i class="bi bi-arrow-right"></i>
              </button>
            </div>
          </div>
        </div>

        <!-- Carousel Column -->
        <div class="col-lg-8 team-carousel-wrap">
          <Swiper
            :modules="[Navigation, Autoplay]"
            :loop="true"
            :speed="800"
            :autoplay="{ delay: 5000 }"
            :slides-per-view="1"
            :space-between="20"
            :navigation="{ nextEl: nextEl, prevEl: prevEl }"
            :breakpoints="{
              576: { slidesPerView: 2, spaceBetween: 20 },
              992: { slidesPerView: 2, spaceBetween: 30 }
            }"
            class="team-carousel"
          >
            <SwiperSlide v-for="member in teamMembers" :key="member.name">
              <div class="member-card">
                <div class="member-image">
                  <img :src="member.image" class="img-fluid" alt="" loading="lazy" />
                </div>
                <div class="member-info">
                  <h3>{{ member.name }}</h3>
                  <span>{{ member.role }}</span>
                  <div class="member-social">
                    <a href="#"><i class="bi bi-twitter-x"></i></a>
                    <a href="#"><i class="bi bi-facebook"></i></a>
                    <a href="#"><i class="bi bi-linkedin"></i></a>
                  </div>
                  <div class="member-bio">
                    <p>{{ member.bio }}</p>
                  </div>
                </div>
              </div>
            </SwiperSlide>
          </Swiper>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, onMounted } from 'vue'
import { Swiper, SwiperSlide } from 'swiper/vue'
import { Navigation, Autoplay } from 'swiper/modules'

import 'swiper/css'
import 'swiper/css/navigation'

const prevEl = ref(null)
const nextEl = ref(null)

const teamMembers = [
  {
    name: 'Marcus Wilson',
    role: 'Chief Technology Officer',
    image: 'src/assets/img/person/person-m-3.webp',
    bio: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut elit tellus, luctus nec ullamcorper mattis.',
  },
  {
    name: 'Sophia Reynolds',
    role: 'Product Designer',
    image: 'src/assets/img/person/person-f-5.webp',
    bio: 'Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.',
  },
  {
    name: 'Daniel Chen',
    role: 'Marketing Specialist',
    image: 'src/assets/img/person/person-m-8.webp',
    bio: 'Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
  },
  {
    name: 'Olivia Thompson',
    role: 'Lead Developer',
    image: 'src/assets/img/person/person-f-9.webp',
    bio: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium.',
  },
  {
    name: 'Jason Parker',
    role: 'UI/UX Designer',
    image: 'src/assets/img/person/person-m-12.webp',
    bio: 'Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni.',
  },
]
</script>

<style scoped>
.team-carousel {
  padding-top: 20px;
}

.member-card {
  border: 1px solid #eee;
  border-radius: 12px;
  overflow: hidden;
  background: #fff;
  padding: 16px;
}
.member-info h3 {
  margin-top: 1rem;
  font-size: 1.25rem;
}
.member-social a {
  margin-right: 8px;
  color: #555;
}
</style>

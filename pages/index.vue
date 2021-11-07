<template>
  <div>
    <TheHero />

    <!-- Контент сайта Section 1 -->
    <section class="text-gray-600 body-font">
      <div class="container px-5 py-24 mx-auto">
        <div class="flex flex-wrap w-full mb-20">
          <div class="lg:w-1/2 w-full mb-6 lg:mb-0">
            <h1
              class="sm:text-3xl text-2xl font-medium title-font mb-2 text-gray-900"
            >Pitchfork Kickstarter Taxidermy</h1>
            <div class="h-1 w-20 bg-indigo-500 rounded"></div>
          </div>
          <p
            class="lg:w-1/2 w-full leading-relaxed text-gray-500"
          >Whatever cardigan tote bag tumblr hexagon brooklyn asymmetrical gentrify, subway tile poke farm-to-table. Franzen you probably haven't heard of them man bun deep jianbing selfies heirloom prism food truck ugh squid celiac humblebrag.</p>
        </div>
        <client-only placeholder="Loading...">
          <!-- important to add no-ssr-->
          <carousel
            :margin="32"
            :nav="true"
            :autoplay="true"
            :autoplayHoverPause="true"
            :responsive="{
              0: { items: 1, nav: false },
              540: { items: 2, nav: true },
              1024: { items:3, nav: true},
              1280: { items: 4, nav: true },
              1920: { items: 4, nav: true }
            }"
          >
            <div
              v-for="CarouselItem in CarouselItems"
              :key="CarouselItem.index"
              class="bg-indigo-100 p-6 rounded-lg"
            >
              <nuxt-img
                class="h-40 rounded w-full object-cover object-center mb-6"
                provider="cloudinary"
                :src="(CarouselItem.img)"
                alt="content"
                width="302" height="160"
                fit="cover"
              />
              <h3
                class="tracking-widest text-indigo-500 text-xs font-medium title-font uppercase"
              >{{ CarouselItem.subtitle }}</h3>
              <h2 class="text-lg text-gray-900 font-medium title-font mb-4">{{ CarouselItem.title }}</h2>
              <p class="leading-relaxed text-base">{{ CarouselItem.description }}</p>
            </div>
          </carousel>
        </client-only>
        <!-- <div class="flex flex-wrap -m-4">
          <div class="xl:w-1/4 md:w-1/2 p-4">
            <div class="bg-indigo-100 p-6 rounded-lg">
              <img
                class="h-40 rounded w-full object-cover object-center mb-6"
                src="https://res.cloudinary.com/poliweb/image/upload/v1636096462/Fashen/catwalk_1920_dgoled.jpg"
                alt="content"
              />
              <h3 class="tracking-widest text-indigo-500 text-xs font-medium title-font">SUBTITLE</h3>
              <h2 class="text-lg text-gray-900 font-medium title-font mb-4">Chichen Itza</h2>
              <p
                class="leading-relaxed text-base"
              >Fingerstache flexitarian street art 8-bit waistcoat. Distillery hexagon disrupt edison bulbche.</p>
            </div>
          </div>
          <div class="xl:w-1/4 md:w-1/2 p-4">
            <div class="bg-indigo-100 p-6 rounded-lg">
              <img
                class="h-40 rounded w-full object-cover object-center mb-6"
                src="https://res.cloudinary.com/poliweb/image/upload/v1636094400/Fashen/fashion-3_1920_j5gq8i.jpg"
                alt="content"
              />
              <h3 class="tracking-widest text-indigo-500 text-xs font-medium title-font">SUBTITLE</h3>
              <h2 class="text-lg text-gray-900 font-medium title-font mb-4">Colosseum Roma</h2>
              <p
                class="leading-relaxed text-base"
              >Fingerstache flexitarian street art 8-bit waistcoat. Distillery hexagon disrupt edison bulbche.</p>
            </div>
          </div>
          <div class="xl:w-1/4 md:w-1/2 p-4">
            <div class="bg-indigo-100 p-6 rounded-lg">
              <img
                class="h-40 rounded w-full object-cover object-center mb-6"
                src="https://res.cloudinary.com/poliweb/image/upload/v1636094396/Fashen/hands_1920_mrblxl.jpg"
                alt="content"
              />
              <h3 class="tracking-widest text-indigo-500 text-xs font-medium title-font">SUBTITLE</h3>
              <h2 class="text-lg text-gray-900 font-medium title-font mb-4">Great Pyramid of Giza</h2>
              <p
                class="leading-relaxed text-base"
              >Fingerstache flexitarian street art 8-bit waistcoat. Distillery hexagon disrupt edison bulbche.</p>
            </div>
          </div>
          <div class="xl:w-1/4 md:w-1/2 p-4">
            <div class="bg-indigo-100 p-6 rounded-lg">
              <img
                class="h-40 rounded w-full object-cover object-center mb-6"
                src="https://res.cloudinary.com/poliweb/image/upload/v1636094321/Fashen/woman-2_1920_lsote0.jpg"
                alt="content"
              />
              <h3 class="tracking-widest text-indigo-500 text-xs font-medium title-font">SUBTITLE</h3>
              <h2 class="text-lg text-gray-900 font-medium title-font mb-4">San Francisco</h2>
              <p
                class="leading-relaxed text-base"
              >Fingerstache flexitarian street art 8-bit waistcoat. Distillery hexagon disrupt edison bulbche.</p>
            </div>
          </div>
        </div>-->
      </div>
    </section>
    <!-- //Контент сайта Section 1 -->
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      // CarouselItems: данные для блока "Section 1 carousel"
      CarouselItems: [
        {
          img: "catwalk_1920_dgoled.jpg",
          title: "Title - Заголовок",
          subtitle: "SubTitle",
          description:
            'Enthusiastically disintermediate web-enabled "outside the box" thinking without fully researched.',
        },
        {
          img: "woman-5_1920_xoh24f.jpg",
          title: "Девушка и авто",
          subtitle: "Активный отдых",
          description:
            "Interactively customize maintainable e-business and maintainable web-readiness. Dynamically cultivate wireless.",
        },
        {
          img: "woman-2_1920_lsote0.jpg",
          title: "Девушка на авто",
          subtitle: "Активный летний отдых",
          description:
            "Phosfluorescently extend intuitive infomediaries via reliable systems. Completely grow covalent.",
        },
        {
          img: "girl-2_1920_r09dll.jpg",
          title: "Девушка и мотоцикл",
          subtitle: "Отдых на мотоцикле",
          description:
            "Synergistically transform transparent channels through principle-centered vortals. Dynamically grow 2.0.",
        },
        {
          img: "hands_1920_mrblxl.jpg",
          title: "Ручные часы",
          subtitle: "Течение времени",
          description:
            "Credibly exploit efficient technologies and fully tested scenarios. Assertively myocardinate.",
        },
        {
          img: "neckties_1920_ykn7ky.jpg",
          title: "Галстук на каждый день",
          subtitle: "Цветовое разнообразие",
          description:
            "Phosfluorescently revolutionize high standards in synergy and multidisciplinary results. Uniquely.",
        },
        {
          img: "wrist-watch_1920_mkat4p.jpg",
          title: "Подарок для мужчины",
          subtitle: "Активный подход к выбору",
          description:
            "Progressively administrate principle-centered niche markets without long-term high-impact interfaces. Objectively.",
        },
        {
          img: "man_1920_pavzmx.jpg",
          title: "Мужчина и авто",
          subtitle: "Активный отдых",
          description:
            "Continually leverage existing worldwide solutions through low-risk high-yield strategic theme.",
        },
      ],
    };
  },
};
</script>

<style>
.owl-carousel .owl-nav button.owl-prev,
.owl-carousel .owl-nav button.owl-next {
  color: inherit;
  border: none;
  padding: 0 !important;
  font: inherit;
  font-size: 28px;
  transition: all 0.3s ease-out;
}

.owl-theme .owl-nav [class*="owl-"] {
  margin: 16px;
  display: inline-block;
  cursor: pointer;
  border-radius: 3px;
}

.owl-theme .owl-nav {
  margin-top: 24px;
  text-align: center;
  -webkit-tap-highlight-color: transparent;
}

.owl-theme .owl-nav [class*="owl-"]:hover {
  background: coral;
  color: #fff;
  text-decoration: none;
}

.owl-theme .owl-nav [class*="owl-"] span {
  padding: 0px 20px;
}

.owl-theme .owl-dots .owl-dot span {
  width: 10px;
  height: 10px;
  margin: 5px 7px;
  background: rgba(255, 127, 80, 0.5);
  display: block;
  -webkit-backface-visibility: visible;
  transition: opacity 200ms ease;
  border-radius: 30px;
}
.owl-theme .owl-dots .owl-dot.active span,
.owl-theme .owl-dots .owl-dot:hover span {
  background: coral;
}
</style>

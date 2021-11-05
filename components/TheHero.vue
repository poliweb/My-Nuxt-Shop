<template>
  <div>
    <client-only placeholder="Loading...">
      <agile>
        <section class="animation-style-01 text-gray-600 body-font bg-purple-700">
          <div class="container mx-auto flex px-5 py-24 md:flex-row flex-col items-center">
            <div class="slide-content lg:max-w-lg lg:w-full md:w-1/2 w-5/6 mb-10 md:mb-0">
              <img
                class="object-cover object-center rounded"
                alt="hero"
                src="https://res.cloudinary.com/poliweb/image/upload/v1636034513/Shop/girl_1920_inkahz.jpg"
              />
            </div>
            <div
              class="slide-content lg:flex-grow md:w-1/2 lg:pl-24 md:pl-16 flex flex-col md:items-start md:text-left items-center text-center"
            >
              <h1 class="title title-font sm:text-4xl text-3xl mb-4 font-medium text-gray-300">
                Before they sold out
                <br class="hidden lg:inline-block" />readymade gluten
              </h1>
              <p
                class="sub-title mb-8 leading-relaxed text-white"
              >Copper mug try-hard pitchfork pour-over freegan heirloom neutra air plant cold-pressed tacos poke beard tote bag. Heirloom echo park mlkshk tote bag selvage hot chicken authentic tumeric truffaut hexagon try-hard chambray.</p>
              <div class="button-wrap flex justify-center">
                <NuxtLink to="/"
                  class="inline-flex text-white bg-coral border-0 py-2 px-6 transition duration-500 ease-in-out  focus:outline-none hover:bg-indigo-600 rounded text-lg"
                >Button</NuxtLink>
                <NuxtLink to=""
                  class="ml-4 inline-flex text-gray-700 bg-gray-100 border-0 py-2 px-6 transition duration-500 ease-in-out  focus:outline-none hover:bg-gray-200 rounded text-lg"
                >Button</NuxtLink>
              </div>
            </div>
          </div>
        </section>
        <section class="animation-style-01 text-gray-600 body-font bg-pink-700">
          <div class="container mx-auto flex px-5 py-24 md:flex-row flex-col items-center">
            <div class="slide-content lg:max-w-lg lg:w-full md:w-1/2 w-5/6 mb-10 md:mb-0">
              <img
                class="object-cover object-center rounded"
                alt="hero"
                src="https://res.cloudinary.com/poliweb/image/upload/v1636034548/Shop/women-office_1920_gbo0eb.jpg"
              />
            </div>
            <div
              class="slide-content lg:flex-grow md:w-1/2 lg:pl-24 md:pl-16 flex flex-col md:items-start md:text-left items-center text-center"
            >
              <h1 class="title title-font sm:text-4xl text-3xl mb-4 font-medium text-gray-300">
                Early black
                <br class="hidden lg:inline-block" />friday deals
              </h1>
              <p
                class="sub-title mb-8 leading-relaxed text-white"
              >Synergistically expedite innovative internal or "organic" sources for plug-and-play quality vectors. Efficiently predominate distinctive alignments vis-a-vis end-to-end niche markets.</p>
              <div class="button-wrap flex justify-center">
                <NuxtLink to=""
                  class="inline-flex text-white bg-coral border-0 py-2 px-6 transition duration-500 ease-in-out  focus:outline-none hover:bg-indigo-600 rounded text-lg"
                >Button</NuxtLink>
                <NuxtLink to=""
                  class="ml-4 inline-flex text-gray-700 bg-gray-100 border-0 py-2 px-6 transition duration-500 ease-in-out  focus:outline-none hover:bg-gray-200 rounded text-lg"
                >Button</NuxtLink>
              </div>
            </div>
          </div>
        </section>
         <!-- Button PREV and NEXT -->
       <template slot="prevButton"
        ><button class="prev">&#10094;</button></template
      >
      <template slot="nextButton"
        ><button class="next">&#10095;</button></template
      >
      </agile>
    </client-only>
  </div>
</template>

<script>
export default {};
</script>

<style>
/* Animation */
.animation-style-01.agile__slide--active .container .slide-content img {
  animation-name: fadeInDown;
  animation-delay: 0.5s;
  animation-duration: 1s;
  animation-fill-mode: both;
}
.animation-style-01.agile__slide--active .container .slide-content .title {
  animation-name: fadeInUp;
  animation-delay: 0.8s;
  animation-duration: 1s;
  animation-fill-mode: both;
}
.animation-style-01.agile__slide--active .container .slide-content .sub-title {
  animation-name: fadeInUp;
  animation-delay: 1.2s;
  animation-duration: 1s;
  animation-fill-mode: both;
}
.animation-style-01.agile__slide--active
  .container
  .slide-content
  .button-wrap
  a:first-child {
  animation-name: fadeInUp;
  animation-delay: 2s;
  animation-duration: 1s;
  animation-fill-mode: both;
}
.animation-style-01.agile__slide--active
  .container
  .slide-content
  .button-wrap
  a:nth-child(2) {
  animation-name: fadeInUp;
  animation-delay: 2.5s;
  animation-duration: 1s;
  animation-fill-mode: both;
}

.agile__slide--active .container .slide-content > :nth-child(4) {
  animation-delay: 1.8s;
}
.agile__slide .container .slide-content {
  opacity: 0;
}
.agile__slide.agile__slide--active .container .slide-content {
  opacity: 1;
}
/* //Animation */
/* Next & previous buttons */
.prev,
.next {
  cursor: pointer;
  position: absolute;
  top: 50%;
  width: auto;
  margin-top: -22px;
  padding: 16px;
  color: #ff5e13;
  font-weight: bold;
  font-size: 24px;
  transition: 0.6s ease;
  border-radius: 0 3px 3px 0;
  user-select: none;
  z-index: 15;
  opacity: 0;
}
.agile:hover .agile__actions .agile__nav-button .prev,
.agile:hover .agile__actions .agile__nav-button .next {
  opacity: 1;
}
/* Position the "next button" to the right */
.next {
  right: 0;
  border-radius: 3px 0 0 3px;
}
/* On hover, add a black background color with a little bit see-through */
.prev:hover,
.next:hover {
  background-color: rgba(0, 0, 0, 0.8);
}
/*  */
</style>

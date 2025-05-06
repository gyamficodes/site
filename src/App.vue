<template>
  <section class=" h-screen  overflow-y-hiden  bg-tona-dark-300 flex flex-col px-3">
    <div class="flex-1 bg-hero">
      <div class="page-view xl:w-[1320px] mx-auto">
        <div class=" lg:py-10   ">
          <div class="flex-items-between">
            <div class="flex-items-center gap-10">
              <h3 class="text-white text-[25px] font-bold cursor-pointer">Gyamficodes</h3>
              <!-- icon view start -->
              <div class="flex-items-center gap-3  hidden lg:flex">
                <i class="lni lni-envelope text-tona-blue text-[28px]"></i>

                <span class="  text-indigo-200">gyamfijohn08@gmail.com</span>
              </div>

              <!-- icon view end -->

              <!-- icon view start -->
              <div class="flex-items-center gap-3  hidden lg:flex">

                <i class="lni lni-phone text-tona-blue text-[28px]"></i>
                <span class=" text-indigo-200">+233 539214630</span>
              </div>
              <!-- icon view end -->

            </div>
            <div class="flex-items-center gap-4  hidden  lg:flex">
              <!-- icon box start -->
              <div
                class="w-[40px] h-[40px] bg-tona-dark-200 rounded-lg flex-items-full-center cursor-pointer  text-indigo-200 hover:bg-tona-blue hover:text-white">
                <a href="https://github.com/gyamficodes" class=" flex items-center justify-center"> <i
                    class="lni lni-github-original"></i></a>
              </div>
              <!-- icon box end -->


              <!-- icon box end -->

              <!-- icon box start -->
              <div
                class="w-[40px] h-[40px] bg-tona-dark-200 rounded-lg flex-items-full-center cursor-pointer  text-indigo-200 hover:bg-tona-blue hover:text-white">
                <a href="https://www.linkedin.com/in/gyamfi-john-23aa5727b/" class=" flex items-center justify-center">
                  <i class="lni lni-linkedin-original"></i></a>
              </div>
              <!-- icon box end -->

              <!-- icon box start -->
              <div
                class="w-[40px] h-[40px] bg-tona-dark-200 rounded-lg flex-items-full-center cursor-pointer  text-indigo-200 hover:bg-tona-blue hover:text-white">
                <a href="mailto:gyamfijohn08@gmail.com" class=" flex items-center justify-center"> <i
                    class="lni lni-envelope "></i></a>
              </div>


              <!-- icon box start -->
              <div
                class="w-[40px] h-[40px] bg-tona-dark-200 rounded-lg flex-items-full-center cursor-pointer  text-indigo-200 hover:bg-tona-blue hover:text-white">
                <a href="https://www.instagram.com/gyamficodes_tech" class=" flex items-center justify-center"> <i
                    class="lni lni-instagram"></i></a>
              </div>
              <!-- icon box end -->


            </div>
            <!-- menu-icon start -->
            <div @click="handdleChangeIcon"
              class=" w-[45px] h-[45px] border border-[#FFFFFF1A] flex items-center justify-center cursor-pointer    lg:hidden rounded-md relative ">
              <i class="lni lni-menu   text-white text-[30px]" v-if="showIcon"></i>
              <i class="lni lni-close   text-white text-[30px]" v-else></i>

            </div>

            <!-- menu-icon start -->
          </div>
        </div>
        <div class="relative lg:hidden">
          <!-- mobile side bar start -->
          <div class=" absolute right-0 top-0 ">
            <div class=" flex flex-col  overflow-hidden relative  z-[999]">
              <div @click="handleScrollToView('.body-view')"
                :class="{ 'translate-x-72': showIcon, '-translate-x-0': !showIcon }"
                class=" h-[55px] w-[250px] cursor-pointer sm:w-[300px]  rounded-lg rounded-r-none px-3 flex  items-center bg-blue-700 font-[600] capitalize  group text-white  transition-all duration-700">
                <span class=" transition-all duration-150 group-hover:translate-x-3">Home</span>
              </div>
              <!-- <div @click="handleScrollToView('.feature-view')"
                :class="{ 'translate-x-72': showIcon, '-translate-x-0': !showIcon }"
                class=" h-[55px] w-[250px] cursor-pointer  sm:w-[300px] rounded-lg rounded-r-none px-3 flex  items-center bg-blue-700 font-[600] capitalize  group text-white   transition-all duration-500">
                <span class=" transition-all duration-150 group-hover:translate-x-3">services</span>
              </div> -->
              <div @click="handleScrollToView('#esp-view')"
                :class="{ 'translate-x-72': showIcon, '-translate-x-0': !showIcon }"
                class=" h-[55px] w-[250px] cursor-pointer  sm:w-[300px] rounded-lg rounded-r-none px-3 flex  items-center bg-blue-700 font-[600]  group text-white   transition-all duration-300">
                <span class=" transition-all duration-150 group-hover:translate-x-3">about me</span>
              </div>
              <div @click="handleScrollToView('.skill-view')"
                :class="{ 'translate-x-72': showIcon, '-translate-x-0': !showIcon }"
                class=" h-[55px] w-[250px] cursor-pointer sm:w-[300px] rounded-lg rounded-r-none px-3 flex  items-center bg-blue-700 font-[600] capitalize group text-white   transition-all duration-200">
                <span class=" transition-all duration-150 group-hover:translate-x-3">skills</span>
              </div>
              <div @click="handleScrollToView('.project-view')"
                :class="{ 'translate-x-72': showIcon, '-translate-x-0': !showIcon }"
                class=" h-[55px] w-[250px] cursor-pointer  sm:w-[300px] rounded-lg rounded-r-none px-3 flex  items-center bg-blue-700 font-[600] capitalize group text-white   transition-all duration-150">
                <span class=" transition-all duration-150 group-hover:translate-x-3">my projects</span>
              </div>
              <div @click="handleScrollToView('.contact-view')"
                :class="{ 'translate-x-72': showIcon, '-translate-x-0': !showIcon }"
                class=" h-[55px] w-[250px] cursor-pointer sm:w-[300px] rounded-lg rounded-r-none px-3 flex  items-center bg-blue-700 font-[600] capitalize group text-white   transition-all duration-100">
                <span class=" transition-all duration-150 group-hover:translate-x-3">contact me</span>
              </div>
            </div>
          </div>
          <!-- mobile side bar end -->

        </div>
        <div class="relative hidden lg:flex">
          <div
            class="bg-tona-dark-200 w-[92px] border-2 rounded-2xl border-[#293245] absolute -left-[40px] top-[180px] z-10 flex-item-col overflow-hidden">
            <!-- menu start -->
            <div @click="handleScrollToView('.body-view')" title="Home"
              class="h-[92px] w-full flex-items-full-center border-b-2 border-[#293245] text-white cursor-pointer hover:bg-tona-blue ">
              <i class="lni lni-home text-[35px]"></i>
            </div>
            <!-- menu end -->

            <!-- menu start -->
            <div @click="handleScrollToView('.about-view')" title="About"
              class=" h-[92px] w-full flex-items-full-center border-b-2 border-[#293245] text-white cursor-pointer hover:bg-tona-blue ">
              <i class="lni lni-user text-[35px]"></i>
            </div>
            <!-- menu end -->
            <!-- menu start -->
            <div @click="handleScrollToView('.skill-view')"
              class=" h-[92px] w-full flex-items-full-center border-b-2 border-[#293245] text-white cursor-pointer hover:bg-tona-blue ">
              <i class="lni lni-rocket text-[35px]"></i>
            </div>
            <!-- menu end -->

            <!-- menu start -->
            <div @click="handleScrollToView('#esp-view')" title="Esperience"
              class=" h-[92px] w-full flex-items-full-center border-b-2 border-[#293245] text-white cursor-pointer hover:bg-tona-blue ">

              <i class="lni lni-remove-file text-[35px]"></i>
            </div>
            <!-- menu end -->



            <!-- menu start -->
            <div @click="handleScrollToView('.project-view')" title="Project"
              class=" h-[92px] w-full flex-items-full-center border-b-2 border-[#293245] text-white cursor-pointer hover:bg-tona-blue ">

              <i class="lni lni-laptop-phone text-[35px]"></i>
            </div>
            <!-- menu end -->

            <!-- menu start -->
            <!-- <div class=" h-[92px] w-full flex-items-full-center border-b-2 border-[#293245] text-white cursor-pointer hover:bg-tona-blue ">
          
              <i class="lni lni-comments-alt-2 text-[35px]"></i>
          </div> -->
            <!-- menu end -->

            <!-- menu start -->
            <div @click="handleScrollToView('.contact-view')" title="Contact"
              class=" h-[92px] w-full flex-items-full-center text-white cursor-pointer hover:bg-tona-blue ">
              <i class="lni lni-phone text-[35px]"></i>
            </div>
            <!-- menu end -->
          </div>


        </div>
        <div
          class="  h-[80vh] bg-tona-dark-200 w-full   overflow-hidden overflow-y-auto relative  rounded-2xl lg:pl-[56px]  xl:pl-[100px] xl:pr-[50px] py-10">

          <!-- Banner section start -->
          <div class="grid sm:grid-col-1 lg:grid-cols-2 gap-5 w-full ">
            <div class="flex-item-col gap-4  lg:mt-[130px]">
              <div class="flex-items-center">
                <img :src="Wave" alt="wave" />
                <h1 class=" text-[45px] md:text-[55px] font-semibold text-white">
                  Hello, I am
                </h1>

              </div>
              <h1 class="text-[40px] md:text-[40px] font-semibold leading-tight text-white mt-[-25px]">
                Gyamfi John <br />
                <span class="text-primary">Full-Stack Developer</span> | UI/UX Designer
              </h1>

              <p class=" text-[#fff]">My love for design and coding began with open-source web development and a deep
                passion for creating.
                I’m ready to turn your ideas into reality through clean, thoughtful code and creative solutions.</p>

              <div class="flex-items-center flex-col sm:flex-row gap-4">
                <div
                  class="py-2 px-6 w-[100%] sm:w-[150px] flex-items-full-center bg-tona-blue rounded-lg cursor-pointer  hover:bg-blue-500">
                  <a href="mailto:gyamfijohn08@gmail.com"><span class="text-white">Hire Me</span></a>
                </div>
                <div
                  class="py-2 px-6 w-[100%] sm:w-[180px] flex-items-full-center border-[1px] border-white rounded-lg cursor-pointer  hover:bg-tona-blue hover:border-tona-blue">
                  <a href="/Gyamfi John _CV.pdf" download="Gyamfi John _CV.pdf"> <span class="text-white ">Download
                      CV</span></a>
                </div>
              </div>

            </div>
            <div class="relative body-view mt-[70px]">
              <div class=" absolute w-[250px] h-[250px]   rounded-full bg-tona-blue left-[25%] top-[30%] animate-ping">
              </div>
              <img :src="PortFolioImage" alt="portfolio" class="z-[1] relative" />
            </div>
          </div>
          <!-- Banner section end -->

          <!-- Feature section end -->
          <div>

          </div>
          <!-- About section start  -->

          <div class="py-20 about-view">
            <div class="border-b border-[#494C5F] pb-3">
              <h3 class="text-white text-2xl capitalize">about</h3>
            </div>
            <p class="text-[#fff] mt-5"> I am a Full-Stack Developer & UI/UX Designer with 4+ years of experience, based
              in Ghana.
              I specialize in building end-to-end web solutions using HTML, CSS, PHP, Vue.js, React, WordPress,
              PrestaShop, Magento, Joomla, and Umbraco — blending clean design with modern, scalable development.

              With over 3 years of remote work experience collaborating with global teams, I bring strong communication
              skills, deep CMS and eCommerce expertise, and a passion for crafting impactful digital experiences. From
              branding to custom builds, I turn concepts into smart, efficient solutions across industries.</p>

          </div>

          <!-- About section end -->

          <!-- Skils section start -->
          <div class="pt-1 pb-10 skill-view">
            <div class="border-b border-[#494C5F] pb-3">
              <h3 class="text-white text-2xl">Skills</h3>
            </div>
            <ul class="mt-7 grid lg:grid-cols-2 gap-3 gap-y-6">
              <!-- frontend -->
              <div>
                <h1 class="text-[#fff] mb-3">Frontend Tech Stack</h1>
                <div class="flex flex-wrap gap-3">
                  <!-- Existing stack (kept as-is) -->
                  <li><a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">Html</a>
                  </li>
                  <li><a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">CSS</a>
                  </li>
                  <li><a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">Sass</a>
                  </li>
                  <li><a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">Less</a>
                  </li>
                  <li><a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">Bootstrap</a>
                  </li>
                  <li><a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">Javascript</a>
                  </li>
                  <li><a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">Typescript</a>
                  </li>
                  <li><a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">Jquery</a>
                  </li>
                  <li><a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">Webpack</a>
                  </li>
                  <li><a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">Tailwind
                      Css</a></li>
                  <li><a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">Vue</a>
                  </li>
                  <li><a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">Vite</a>
                  </li>
                  <li><a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">Nuxt
                      JS</a></li>
                  <li><a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">Vuex</a>
                  </li>
                  <li><a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">Pinia</a>
                  </li>
                  <li><a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">React</a>
                  </li>
                  <li><a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">Next.Js</a>
                  </li>
                  <li><a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">PrestaShop</a>
                  </li>
                  <li><a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">Redux</a>
                  </li>
                  <li><a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">Redux
                      Saga</a></li>
                  <li><a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">StoryBook</a>
                  </li>


                  <!-- Added based on job description -->
                  <li><a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">WordPress</a>
                  </li>
                  <li><a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">WooCommerce</a>
                  </li>
                  <li><a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">Joomla</a>
                  </li>
                  <li><a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">Magento</a>
                  </li>
                  <li><a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">PrestaShop</a>
                  </li>
                  <li><a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">Umbraco</a>
                  </li>
                </div>

              </div>
              <!-- frontend -->

              <!-- backend -->
              <div>
                <h1 class="text-[#fff] mb-3"> Backend Tech Stack</h1>
                <div class="flex flex-wrap gap-3">

                  <li>
                    <a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">Php</a>
                  </li>
                  <li>
                    <a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">Laravel</a>
                  </li>
                  <li>
                    <a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">Postgresql</a>
                  </li>
                  <li>
                    <a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">Memcached</a>
                  </li>
                  <li>
                    <a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">MYSQL</a>
                  </li>
                  <li>
                    <a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">Redis</a>
                  </li>
                </div>
              </div>
              <!-- backend -->

              <!-- frontend -->
              <div>
                <h1 class="text-[#fff] mb-3">Other Tech Stack</h1>
                <div class="flex flex-wrap gap-3">


                  <li>
                    <a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">GraphQl</a>
                  </li>
                  <li>
                    <a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">Version
                      Control (Git/Github)</a>
                  </li>
                  <li>
                    <a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">Postman</a>
                  </li>
                  <li>
                    <a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">Jira
                      Software</a>
                  </li>
                  <li>
                    <a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">Scrum</a>
                  </li>
                  <li>
                    <a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">Figma</a>
                  </li>
                  <li>
                    <a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">Jest(vitest)</a>
                  </li>
                  <li>
                    <a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">Adobe
                      XD</a>
                  </li>
                  <li>
                    <a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">Adobe
                      Photoshop</a>
                  </li>
                  <li>
                    <a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">Vercel</a>
                  </li>
                  <li>
                    <a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">Nestlify</a>
                  </li>
                  <li>
                    <a href="#"
                      class="bg-[#16213B] block px-4 py-3 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-xl">CI/CD</a>
                  </li>
                </div>
              </div>
              <!-- frontend -->
            </ul>
          </div>
          <!-- Skils section end -->
          <!-- Skils section start -->

          <div id="esp-view" class="py-10">
            <div class="border-b border-[#494C5F] pb-3">
              <h3 class="text-white text-2xl">Experience</h3>
            </div>
            <div class="mt-4">
              <!-- Fennelsoft -->
              <div class="flex lg:flex-row flex-col gap-3">
                <div class="lg:w-[20%]">
                  <h1 class="w-full text-[#fff]">Jun 2023 - Present</h1>
                </div>
                <div class="flex-1">
                  <h1 class="text text-[#fff] mb-2">FennelSoft - Full Stack Developer</h1>
                  <p class="text-[#fff] text-[15px]">
                    <strong>Clefmate Hotel Management SaaS:</strong><br>
                    - Led full-stack development serving 60+ clients, contributing 30% company revenue<br>
                    - Implemented Blazor/TailwindCSS UI that reduced operational costs by 20%<br>
                    - Achieved 90+ Lighthouse scores through optimized architecture<br><br>

                    <strong>Aberfo Business Platform:</strong><br>
                    - Built corporate website using Umbraco CMS with Framer Motion animations<br>
                    - Increased conversions by 27% through performance optimizations<br>
                    - Delivered flawless IE11+ support via custom JavaScript SDK<br><br>

                    <strong>IMA Innovate Maritime Africa:</strong><br>
                    - Developed WordPress website with custom Elementor components<br>
                    - Implemented SEO strategy increasing organic traffic by 30% YoY<br><br>

                    <strong>Developer Training Program:</strong><br>
                    - Launched developer training program (Vue.js, React, Laravel), mentoring 5+ engineers monthly<br>
                    - Produced job-ready hires (2 joined FennelSoft), while generating new revenue streams
                  </p>
                  <div class="flex items-center flex-wrap gap-1 mt-2">
                    <a href="#"
                      class="bg-[#16213B] border block px-1 py-1 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-[14px]">C#/.NET</a>
                    <a href="#"
                      class="bg-[#16213B] block border px-1 py-1 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-[14px]">Umbraco</a>
                    <a href="#"
                      class="bg-[#16213B] border block px-1 py-1 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-[14px]">WordPress</a>
                    <a href="#"
                      class="bg-[#16213B] border block px-1 py-1 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-[14px]">Blazor</a>
                    <a href="#"
                      class="bg-[#16213B] border block px-1 py-1 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-[14px]">TailwindCSS</a>
                  </div>
                </div>
              </div>

              <!-- Ezitek -->
              <div class="flex lg:flex-row flex-col gap-3 mt-5">
                <div class="lg:w-[20%]">
                  <h1 class="w-full text-[#fff]">Apr 2021 - May 2023</h1>
                </div>
                <div class="flex-1">
                  <h1 class="text text-[#fff] mb-2">Eziteck Solution - Frontend Developer</h1>
                  <p class="text-[#fff] text-[15px]">
                    <strong>Ezi Food Platform:</strong><br>
                    - Architected food ordering system serving 50+ restaurants<br>
                    - Integrated Stripe/Paystack payments boosting checkouts by 25%<br>
                    - Reduced API latency by 40% through performance optimizations<br><br>

                    <strong>RAMS Engineering:</strong><br>
                    - Redesigned website with WCAG-compliant UI/UX<br>
                    - Increased leads by 15% through responsive design improvements<br>
                    - Achieved 95+ Lighthouse scores for accessibility
                  </p>
                  <div class="flex items-center flex-wrap gap-1 mt-2">
                    <a href="#"
                      class="bg-[#16213B] border block px-1 py-1 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-[14px]">Vue.js</a>
                    <a href="#"
                      class="bg-[#16213B] block border px-1 py-1 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-[14px]">Laravel</a>
                    <a href="#"
                      class="bg-[#16213B] border block px-1 py-1 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-[14px]">PostgreSQL</a>
                    <a href="#"
                      class="bg-[#16213B] border block px-1 py-1 hover:bg-new-500 hover:text-interface-100 transition duration-300 rounded-md text-white text-[14px]">TailwindCSS</a>
                  </div>
                </div>
              </div>
            </div>
          </div>



          <!-- Skils section end -->


          <!-- Project section -->

          <div class="py-10 project-view">
            <div class="flex flex-col sm:flex-row justify-between gap-4 items-center pb-10">
              <h1 class="sm:w-1/2 w-full text-white font-work font-bold text-3xl sm:text-[42px]">
                Let’s Check <br>
                my Best work
              </h1>

              <!-- <a href="#" class="sm:px-8 px-3 py-3 border border-borderl-500 text-lg font-medium tex rounded-lg">
                      See&nbsp;More
                    </a> -->
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 xl:grid-cols-2 gap-4">
              <div class="group w-full h-[280px] relative cursor-pointer">
                <div
                  class="bg-[#000000d7] absolute w-full h-0 flex items-center overflow-hidden justify-center flex-col gap-2 px-5 text-center transition-all ease-in-out duration-300 group-hover:h-full">
                  <h3 class="text-white font-bold text-[25px]">ClefMate Hotel SaaS</h3>
                  <span class="text-white text-[13px] sm:text-s">
                    Comprehensive hotel management platform serving 60+ clients, contributing 30% of company revenue
                    with 98% retention rate.
                  </span>
                  <span class="text-white text-[15px] sm:text-sm">
                    Tech Stack: C#/.NET, Blazor, Umbraco CMS, Tailwind CSS, JavaScript, jQuery, MSSQL
                  </span>
                  <div class="flex flex-wrap justify-center gap-2 mt-2">
                    <span class="bg-[#ffffff20] px-2 py-1 rounded-full text-white text-xs">90+ Lighthouse</span>
                    <span class="bg-[#ffffff20] px-2 py-1 rounded-full text-white text-xs">20% Cost Reduction</span>
                    <span class="bg-[#ffffff20] px-2 py-1 rounded-full text-white text-xs">99.9% Uptime</span>
                  </div>
                  <div class="mt-4 flex gap-4">
            <a class="border-2 border-new-500 bg-new-500/10 hover:bg-new-500 rounded-md px-6 py-2 text-sm font-medium text-white hover:text-white transition-all duration-300 flex items-center gap-1"
               href="https://app.clefmate.com/account/login" target="_blank" rel="noopener noreferrer">
                Live Demo
                <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14"></path>
                </svg>
            </a>
           
        </div>
                </div>
                <img class="w-full h-full object-cover" :src="clefmate"
                  alt="ClefMate Hotel Management System dashboard" />
              </div>

              <div class="group w-full h-[240px] relative cursor-pointer">
                <div
                  class="bg-[#000000d7] absolute w-full h-0 flex items-center overflow-hidden justify-center flex-col gap-2 px-5 text-center transition-all ease-in-out duration-300 group-hover:h-full">
                  <h3 class="text-white font-bold text-[25px]">IMA Innovate Maritime Africa</h3>
                  <span class="text-white text-[13px] sm:text-sm">
                    Developed a dynamic WordPress website with custom Elementor components to showcase IMA's mission of
                    empowering Africa's maritime sector through innovation and entrepreneurship. Implemented SEO
                    strategies that increased organic traffic by 30% year-over-year.
                  </span>
                  <span class="text-white text-[15px] sm:text-sm">
                    <strong>Tech Stack:</strong> WordPress, Elementor, SEO Optimization
                  </span>
                  <a class="mt-2 border border-new-500 rounded-md px-8 py-2 text-sm text-white gallery"
                    href="https://innovatemaritimeafrica.com/">View Project</a>
                </div>
                <img class="w-full h-full object-cover" :src="imaProjectImage"
                  alt="IMA Innovate Maritime Africa Project" />
              </div>

              <div class="group w-full h-[280px] relative cursor-pointer">
                <div
                  class="bg-[#000000d7] absolute w-full h-0 flex items-center overflow-hidden justify-center flex-col gap-2 px-5 text-center transition-all ease-in-out duration-300 group-hover:h-full">
                  <h3 class="text-white font-bold text-[25px]">Fennelsoft</h3>
                  <span class="text-white text-[13px] sm:text-s">
                    Developed enterprise solutions using Umbraco CMS at Fennelsoft, creating performant websites with
                    95+ Lighthouse scores and 27% conversion improvements.
                  </span>
                  <span class="text-white text-[15px] sm:text-sm">
                    Tech Stack: Umbraco CMS, Tailwind CSS, JavaScript, jQuery, Blazor (C#), .NET, Azure DevOps
                  </span>
                  <div class="flex flex-wrap justify-center gap-2 mt-2">
                    <span class="bg-[#ffffff20] px-2 py-1 rounded-full text-white text-xs">CMS Development</span>
                    <span class="bg-[#ffffff20] px-2 py-1 rounded-full text-white text-xs">Performance
                      Optimization</span>
                  </div>
                  <a class="mt-4 border border-new-500 rounded-md px-8 py-2 text-sm text-white gallery hover:bg-new-500 hover:text-white transition-colors duration-300"
                    href="https://fennelsoft.com" target="_blank">View Project</a>
                </div>
                <img class="w-full h-full object-cover" :src="fennel" alt="Fennelsoft website built with Umbraco CMS" />
              </div>



              <div class="group w-full h-[280px] relative cursor-pointer">
                <div
                  class="bg-[#000000d7] absolute w-full h-0 flex items-center overflow-hidden justify-center flex-col gap-2 px-5 text-center transition-all ease-in-out duration-300 group-hover:h-full">
                  <h3 class="text-white font-bold text-[20px] sm:text-[25px]">EZI FOOD Platform</h3>
                  <span class="text-white text-[13px] sm:text-sm">
                    Architected food ordering system serving 50+ restaurants with real-time tracking, reducing API
                    latency by 40% and boosting checkout completions by 25%.
                  </span>
                  <span class="text-white text-[15px] sm:text-sm">
                    Tech Stack: Vue.js, Laravel, PostgreSQL, Stripe/Paystack, TailwindCSS
                  </span>
                  <div class="flex flex-wrap justify-center gap-2 mt-2">
                    <span class="bg-[#ffffff20] px-2 py-1 rounded-full text-white text-xs">50+ Restaurants</span>
                    <span class="bg-[#ffffff20] px-2 py-1 rounded-full text-white text-xs">40% Latency Reduction</span>
                    <span class="bg-[#ffffff20] px-2 py-1 rounded-full text-white text-xs">25% More Checkouts</span>
                  </div>
                  <a class="mt-4 border border-new-500 rounded-md px-8 py-2 text-sm text-white gallery hover:bg-new-500 hover:text-white transition-colors duration-300"
                    href="https://www.ezifood.com/location" target="_blank">View Project</a>
                </div>
                <img class="w-full h-full object-cover" :src="Ezi" alt="EZI FOOD online ordering platform" />
              </div>




              <div class="group w-full h-[280px] relative cursor-pointer">
                <div
                  class="bg-[#000000d7] absolute w-full h-0 flex items-center overflow-hidden justify-center flex-col gap-2 px-5 text-center transition-all ease-in-out duration-300 group-hover:h-full">
                  <h3 class="text-white font-bold text-[25px]">Aberfo Business Platform</h3>
                  <span class="text-white text-[13px] sm:text-s">
                    Corporate website built with Umbraco CMS featuring dynamic animations and 27% conversion rate
                    improvement.
                  </span>
                  <span class="text-white text-[15px] sm:text-sm">
                    Tech Stack: Umbraco CMS, Tailwind CSS, JavaScript, jQuery, Framer Motion
                  </span>
                  <div class="flex flex-wrap justify-center gap-2 mt-2">
                    <span class="bg-[#ffffff20] px-2 py-1 rounded-full text-white text-xs">27% Conversions</span>
                    <span class="bg-[#ffffff20] px-2 py-1 rounded-full text-white text-xs">95+ Lighthouse</span>
                    <span class="bg-[#ffffff20] px-2 py-1 rounded-full text-white text-xs">IE11 Support</span>
                  </div>
                  <a class="mt-4 border border-new-500 rounded-md px-8 py-2 text-sm text-white gallery hover:bg-new-500 hover:text-white transition-colors duration-300"
                    href="https://aberfo.com" target="_blank">View Project</a>
                </div>
                <img class="w-full h-full object-cover" :src="Aberfo"
                  alt="Aberfo corporate website built with Umbraco CMS" />
              </div>



              <div class="group w-full h-[280px] relative cursor-pointer">
                <div
                  class="bg-[#000000d7] absolute w-full h-0 flex items-center overflow-hidden justify-center flex-col gap-2 px-5 text-center transition-all ease-in-out duration-300 group-hover:h-full">
                  <h3 class="text-white font-bold text-[20px] sm:text-[25px]">RAMS Engineering</h3>
                  <span class="text-white text-[13px] sm:text-sm">
                    Redesigned corporate website with WCAG-compliant UI/UX, increasing leads by 15% while achieving 95+
                    Lighthouse scores.
                  </span>
                  <span class="text-white text-[15px] sm:text-sm">
                    Tech Stack: HTML5, CSS3, JavaScript, jQuery, TailwindCSS
                  </span>
                  <div class="flex flex-wrap justify-center gap-2 mt-2">
                    <span class="bg-[#ffffff20] px-2 py-1 rounded-full text-white text-xs">WCAG 2.1 AA</span>
                    <span class="bg-[#ffffff20] px-2 py-1 rounded-full text-white text-xs">15% Lead Increase</span>
                    <span class="bg-[#ffffff20] px-2 py-1 rounded-full text-white text-xs">95+ Scores</span>
                  </div>
                  <a class="mt-4 border border-new-500 rounded-md px-8 py-2 text-sm text-white gallery hover:bg-new-500 hover:text-white transition-colors duration-300"
                    href="https://www.reamc.com/" target="_blank">View Project</a>
                </div>
                <img class="w-full h-full object-cover" :src="contact" alt="RAMS Engineering WCAG-compliant website" />
              </div>
              <div class="group w-full h-[240px] relative cursor-pointer ">
                <div
                  class=" bg-[#000000d7] absolute w-full h-0 flex items-center overflow-hidden justify-center flex-col gap-2 px-5 text-center transition-all ease-in-out duration-300 group-hover:h-full">
                  <h3 class="text-white font-bold text-[15px] sm:text-[25px]">Ecormence Advance Filtering App</h3>
                  <span class="text-white ">Experience seamless online shopping with my advanced e-commerce filter app,
                    a side project built with React, Tailwind CSS, and JavaScript. It offers personalized product
                    searches for a streamlined shopping experience.</span>
                  <span class="text-white text-[15px] sm:text-sm"> Tech Stack: React ,Tailwind Css, Javascript </span>
                  <a class="mt- border border-new-500 rounded-md px-8 py-2 text-sm text-white gallery"
                    href="https://e-commerce-advance-filtering-dusky.vercel.app/">View Project</a>
                </div>
                <img class="w-full h-full object-cover" :src="Ecor" alt="project" />
              </div>

              <div class="group w-full h-[300px] relative cursor-pointer">
                <div
                  class="bg-[#000000d7] absolute w-full h-0 flex items-center overflow-hidden justify-center flex-col gap-2 px-5 text-center transition-all ease-in-out duration-300 group-hover:h-full">
                  <h3 class="text-white font-bold text-[22px] sm:text-[26px]">Kofi Aberfo Business Platform</h3>
                  <span class="text-white text-[14px] sm:text-sm">
                    Corporate website built with Umbraco CMS featuring dynamic Framer Motion animations that increased
                    conversions by 27% and achieved 95+ Lighthouse scores.
                  </span>
                  <span class="text-white text-[15px] sm:text-sm">
                    Tech Stack: Umbraco CMS, Tailwind CSS, JavaScript, jQuery, Framer Motion
                  </span>
                  <div class="flex flex-wrap justify-center gap-2 mt-3">
                    <span class="bg-[#ffffff20] px-3 py-1 rounded-full text-white text-xs">27% Conversion Boost</span>
                    <span class="bg-[#ffffff20] px-3 py-1 rounded-full text-white text-xs">95+ Performance</span>
                    <span class="bg-[#ffffff20] px-3 py-1 rounded-full text-white text-xs">Cross-Browser</span>
                  </div>
                  <a class="mt-5 border-2 border-new-500 rounded-md px-8 py-2 text-sm font-medium text-white hover:bg-new-500 hover:text-white transition-all duration-300"
                    href="https://kofiaberfo.com/" target="_blank" rel="noopener noreferrer">
                    Visit Website
                  </a>
                </div>
                <img class="w-full h-full object-cover" :src="tech"
                  alt="Kofi Aberfo corporate website built with Umbraco CMS" />
              </div>

            </div>
          </div>

          <!-- Project section end -->


          <!-- contact section start -->
          <div class="py-10 contact-view text-center">
            <h1 class="text-[40px] text-center text-white font-bold">Say Hello!</h1>
            <p class="text-center  text-white lg:w-[50%]  mx-auto mt-2">Get in touch and discover how I can contribute
              to the growth of your business and team.</p>
            <div
              class="animating mt-5 w-[50px] h-[50px] mx-auto rounded-full flex items-center justify-center border border-white">
              <i class="lni lni-arrow-down text-white "></i>
            </div>
            <button
              class=" w-[180px] h-[50px] border mt-2 rounded-xl capitalize cursor-pointer text-white hover:bg-tona-blue hover:border-tona-blue">
              <a href="mailto:gyamfijohn08@gmail.com">say hello!</a>
            </button>
          </div>
          <!-- Contact section end -->
        </div>
      </div>
    </div>
    <div class="h-[70px] border-t border-[#121B30]">
      <p class="py-4 text-white font-medium text-base md:text-lg font-work text-center">
        Copyright © {{ new Date().getFullYear() }} – All Rights Reserved

      </p>
    </div>
  </section>
</template>

<script setup lang="ts">
import PortFolioImage from './assets/Images/model.png'
import fennelsoft from "./assets/Images/project/fennesoft.png"
import Wave from './assets/Images/waving-hand.svg'
import clef from "./assets/Images/project/clefmate.png";
import Ezi from "./assets/Images/project/EziFood.png";
import imaProjectImage from "./assets/Images/project/safe.png";
import contact from "./assets/Images/project/contact.png";
import sika from "./assets/Images/project/sikapa.png";
import clefmate from "./assets/Images/project/friday.png";
import Ecormence from "./assets/Images/project/Ecormence.png";
import Aberfo from "./assets/Images/project/aberfo.png";
import tech from "./assets/Images/project/tech.png";
import { ref } from 'vue'

const showIcon = ref<boolean>(true);
const fennel = ref<string>(fennelsoft)
const Ecor = ref<string>(Ecormence);

function handdleChangeIcon() {
  showIcon.value = !showIcon.value;
}

const handleScrollToView = (className: string) => {
  const element = document.querySelector(className)
  element?.scrollIntoView({ behavior: 'smooth' })
}
</script>


<style scoped>
.animating {
  animation: move 1s linear infinite;
}

@keyframes move {
  0% {
    transform: translateY(-10px);
  }

  50% {
    transform: translateY(0px);
  }

  100% {
    transform: translateY(-10px);
  }
}
</style>

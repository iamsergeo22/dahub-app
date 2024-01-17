<template>
  <div class="font-sans tw-opacity-90">


    <header :class="{ 'bg-color': isScrolled }" class="lg:tw-fixed tw-top-0 tw-left-0 tw-right-0 tw-z-50">      
      <div class="tw-block lg:tw-hidden tw-flex-row tw-flex tw-justify-between tw-items-center tw-px-4">
        <div class="">
          <nuxt-link to="/">
            <h1 class="tw-flex lg:tw-text-6xl tw-text-4xl tw-font-extrabold">
              <span class="tw-text-black">Da</span>
              <span class="tw-text-white tw-hidden lg:tw-block">H</span>
              <span class="tw-text-yellow-400 lg:tw-hidden tw-block">H</span>
              <span class="tw-text-black">ub</span>
            </h1>
          </nuxt-link>
        </div>


        <div class="tw-block lg:tw-hidden">
          <button @click="toggleMenu"
            class="tw-flex tw-items-center tw-px-3 tw-py-4 border tw-rounded tw-border-gray-500 hover:tw-border-gray-600">
            <svg class="tw-current-color tw-h-3 tw-w-3" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
              <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" fill="gray" />
            </svg>
          </button>
        </div>
      </div>
      <nav
        class="tw-bg-transparent tw-py-2 lg:tw-py-0 tw-px-4 lg:tw-flex lg:tw-flex-row  lg:tw-justify-evenly lg:tw-mt-1 tw-items-center">

        <div class="lg:tw-block tw-hidden">
          <nuxt-link to="/">
            <h1 class="tw-flex lg:tw-text-6xl tw-text-4xl tw-font-extrabold">
              <span class="tw-text-black">Da</span>
              <span class="tw-text-white tw-hidden lg:tw-block">H</span>
              <span class="tw-text-yellow-400 lg:tw-hidden tw-block">H</span>
              <span class="tw-text-black">ub</span>
            </h1>
          </nuxt-link>
        </div>


        <ul
          class="tw-tracking-wide tw-px-2 tw- tw-w-full tw-block tw-flex-grow lg:tw-space-x-8 tw-space-y-6 lg:tw-space-y-0 lg:tw-flex lg:tw-flex-initial lg:tw-w-auto tw-mt-4 lg:tw-mt-0"
          :class="{ 'tw-block': isOpen, 'tw-hidden': !isOpen }">
          <li class="tw-mb-6 lg:tw-mb-0">
            <!-- <search-input /> -->
          </li>

          <li @click="closeMenu">
            <nuxt-link to="/" :class="$route.path === '/' ? 'active' : ''"
              class="text-black 	hover:text-blue-800 text-md hover:no-underline">Services</nuxt-link>
          </li>


          <li @click="closeMenu">
            <nuxt-link to="/" :class="$route.path === '/' ? 'active' : ''"
              class="text-black 	hover:text-blue-800 text-md hover:no-underline">Works</nuxt-link>
          </li>


          <li @click="closeMenu">
            <nuxt-link to="/" :class="$route.path === '/' ? 'active' : ''"
              class="text-black 	hover:text-blue-800 text-md hover:no-underline">About Us</nuxt-link>
          </li>

        </ul>


        <button
          class="tw-group tw-hidden lg:tw-block tw-bg-gray-100 tw-shadow-lg tw-rounded-lg tw-relative tw-h-12 tw-mt-4 tw-cursor-pointer hover:tw-transform hover:tw-translate-x-2 hover:tw-transition-transform hover:tw-duration-300 hover:tw-shadow-2xl-blue-600 hover:tw-shadow-2xl-lg tw-w-48 tw-overflow-hidden tw-rounded-lg tw-text-lg tw-rounded-rt-full">
          <div
            class="tw-absolute tw-inset-0 tw-w-full tw-bg-gray-100 tw--transition-all tw-duration-[250ms] tw-ease-out group-hover:tw-w-full">
          </div>
          <span class="tw-relative tw-inline-flex tw-items-center tw-gap-2 tw-text-black group-hover:tw-text-black">
            Contacts

          </span>
        </button>

      </nav>


    </header>



    <div class="tw-flex-grow">
      <Nuxt />
    </div>


    <footer class="tw-flex tw-flex-col lg:tw-flex-row tw-p-8 tw-py-12 lg:tw-px-24">

      <div class="tw-mb-8">

        <nuxt-link to="/">
            <h2 class="tw-flex lg:tw-text-6xl tw-text-4xl tw-text-xl tw-font-extrabold">
              <span class="tw-text-black">Da</span>
              <span class="tw-text-yellow-500">H</span>
              <span class="tw-text-black">ub</span>
            </h2>
          </nuxt-link>

          <p class="tw-text-black tw-font-medium lg:tw-text-sm tw-mt-2">
            Lorem ipsum dolor sit amet consectetur. 
          </p>
          <p class="tw-text-black tw-font-medium lg:tw-text-sm tw-mt-2">
            Mattis enim volutpat sed sollicitudin.
          </p>

      </div>

      <v-row class="lg:tw-px-24">
        <v-col class="" cols="6" md="3" lg="3">
          <h1 class="tw-text-black tw-font-extrabold lg:tw-text-xl tw-mt-2 tw-mb-4 tw-items-center">Company</h1>

          <ul
            class="tw-tracking-wide tw-px-2 tw-font-light">
           
            <li class="lg:tw-mb-4">
              <nuxt-link to="/" :class="$route.path === '/' ? 'active' : ''"
                class="text-black 	hover:text-blue-800 text-md hover:no-underline">About Us</nuxt-link>
            </li>


            <li class="lg:tw-mb-4">
              <nuxt-link to="/" :class="$route.path === '/' ? 'active' : ''"
                class="text-black 	hover:text-blue-800 text-md hover:no-underline">Contact</nuxt-link>
            </li>


            <li class="lg:tw-mb-4">
              <nuxt-link to="/" :class="$route.path === '/' ? 'active' : ''"
                class="text-black 	hover:text-blue-800 text-md hover:no-underline">Careers</nuxt-link>
            </li>

          </ul>


        </v-col>

        <v-col class="" cols="6" md="3" lg="63">
          <h1 class="tw-text-black tw-font-extrabold lg:tw-text-xl tw-mt-2 tw-mb-4 tw-items-center">Contact Us</h1>

          <ul
            class="tw-tracking-wide tw-px-2 tw-font-light">
           
            <li class="lg:tw-mb-4">
              <nuxt-link to="/" :class="$route.path === '/' ? 'active' : ''"
                class="text-black 	hover:text-blue-800 text-md hover:no-underline">Website</nuxt-link>
            </li>


            <li class="lg:tw-mb-4">
              <nuxt-link to="/" :class="$route.path === '/' ? 'active' : ''"
                class="text-black 	hover:text-blue-800 text-md hover:no-underline">Email</nuxt-link>
            </li>


    
          </ul>


        </v-col>

        <v-col class="" cols="6" md="3" lg="3">
          <h1 class="tw-text-black tw-font-extrabold lg:tw-text-xl tw-mt-2 tw-mb-4 tw-items-center">Support</h1>

          <ul
            class="tw-tracking-wide tw-px-2">
           

            <li class="lg:tw-mb-4">
              <nuxt-link to="/" :class="$route.path === '/' ? 'active' : ''"
                class="text-black 	hover:text-blue-800 text-md hover:no-underline">FAQ</nuxt-link>
            </li>


            <li class="lg:tw-mb-4">
              <nuxt-link to="/" :class="$route.path === '/' ? 'active' : ''"
                class="text-black 	hover:text-blue-800 text-md hover:no-underline">Working</nuxt-link>
            </li>


            <li class="lg:tw-mb-4">
              <nuxt-link to="/" :class="$route.path === '/' ? 'active' : ''"
                class="text-black 	hover:text-blue-800 text-md hover:no-underline">Guideline</nuxt-link>
            </li>

          </ul>


        </v-col>

        <v-col class="" cols="6" md="3" lg="3">
          <h1 class="tw-text-black tw-font-extrabold lg:tw-text-xl tw-mt-2 tw-mb-4 tw-items-center">Social Media</h1>

          <ul
            class="tw-tracking-wide tw-px-2 tw-gap-4">
          
            <li class="lg:tw-mb-4">
              <nuxt-link to="/" :class="$route.path === '/' ? 'active' : ''"
                class="text-black 	hover:text-blue-800 text-md hover:no-underline">Instagram</nuxt-link>
            </li>


            <li class="lg:tw-mb-4">
              <nuxt-link to="/" :class="$route.path === '/' ? 'active' : ''"
                class="text-black 	hover:text-blue-800 text-md hover:no-underline">Facebook</nuxt-link>
            </li>


            <li class="lg:tw-mb-4">
              <nuxt-link to="/" :class="$route.path === '/' ? 'active' : ''"
                class="text-black 	hover:text-blue-800 text-md hover:no-underline">Youtube</nuxt-link>
            </li>

          </ul>


        </v-col>

      </v-row>

    </footer>

  </div>
</template>


<script>
  export default {
    data() {
      return {
        isOpen: false,
        theme: 'theme-light',
        selectedItem: null,
        isScrolled: false,
      };
    },


    mounted() {
    window.addEventListener('scroll', this.handleScroll);
  },

  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll);
  },

    methods: {

      handleScroll() {
      this.isScrolled = window.scrollY > 0;
    },
      toggleMenu() {
        this.isOpen = !this.isOpen;
      },
      closeMenu() {
        this.isOpen = false;
      },
      closeDialog() {
        this.$emit("close");
      },
      openModal() {
        this.modalVisible = true;
      }

    },



  }

</script>

<style scoped>


  footer {
    background-color: whitesmoke;
  }

  h1 {
    color: #142147;
font-style: normal;
font-weight: 700;
line-height: normal;
  }

  li {
    color: #142147;
font-style: normal;
font-weight: 200;
line-height: normal;
  }


  .text-color {
    color: #FFF500;
  }

  .bg-color {
    background-color: #FFF500;
  }



  .font-sans {
    font-family: 'Josefin Sans', sans-serif;
    font-family: 'Poppins', sans-serif;
  }

</style>

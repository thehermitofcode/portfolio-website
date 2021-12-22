<template>
  <nav class="grid grid-cols-2 mt-7">
    <div>
      <img src="~/assets/img/profile.png" alt="profile-picture" />
    </div>
    <div class="self-center justify-self-end">
      <button
        class="
          font-body font-normal
          py-2
          px-6
          text-sm
          rounded-[12px]
          bg-black
          text-white
          subpixel-antialiased
        "
        @click="isNavOpen = !isNavOpen"
      >
        Menu
      </button>
    </div>
    <transition
      enter-active-class="transition ease-out duration-75"
      enter-from-class="transform opacity-0 scale-95"
      enter-to-class="transform opacity-100 scale-100"
      leave-active-class="transition ease-in duration-75"
      leave-from-class="transform opacity-100 scale-100"
      leave-to-class="transform opacity-0 scale-95"
    >
      <section
        v-if="!isNavOpen"
        class="
          font-body font-bold
          text-sm
          fixed
          z-50
          top-0
          right-0
          overflow-y-auto
        "
      >
      
        <div class="fixed inset-0 backdrop-blur-sm"></div>
        <div
          class="relative bg-white w-80 h-screen max-w-[calc(100% - 3rem)] p-6"
        >
          <div class="flex justify-end">
            <div
              class="
                hover:bg-[#f0f0f0]
                p-4
                w-10
                h-10
                rounded-full
                cursor-pointer
              "
              @click="isNavOpen = !isNavOpen"
            >
              <svg
                width="8"
                height="8"
                viewBox="0 0 8 8"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  fill-rule="evenodd"
                  clip-rule="evenodd"
                  d="M0.195262 0.195262C0.455612 -0.0650874 0.877722 -0.0650874 1.13807 0.195262L4 3.05719L6.86193 0.195262C7.12228 -0.0650874 7.54439 -0.0650874 7.80474 0.195262C8.06509 0.455612 8.06509 0.877722 7.80474 1.13807L4.94281 4L7.80474 6.86193C8.06509 7.12228 8.06509 7.54439 7.80474 7.80474C7.54439 8.06509 7.12228 8.06509 6.86193 7.80474L4 4.94281L1.13807 7.80474C0.877722 8.06509 0.455612 8.06509 0.195262 7.80474C-0.0650874 7.54439 -0.0650874 7.12228 0.195262 6.86193L3.05719 4L0.195262 1.13807C-0.0650874 0.877722 -0.0650874 0.455612 0.195262 0.195262Z"
                  fill="black"
                />
              </svg>
            </div>
          </div>
          <div
            class="
              hover:bg-[#f0f0f0]
              py-2
              mt-6
              pl-4
              rounded-[12px]
              cursor-pointer
            "
          >
            <p>Projects</p>
          </div>
          <div
            class="
              hover:bg-[#f0f0f0]
              py-2
              mt-3
              pl-4
              rounded-[12px]
              cursor-pointer
            "
          >
            <p>Articles</p>
          </div>
          <div
            class="
              hover:bg-[#f0f0f0]
              py-2
              mt-3
              pl-4
              rounded-[12px]
              cursor-pointer
            "
          >
            <a href="https://www.github.com/thehermitofcode" target="_blank">GitHub</a>
          </div>
          <div
            class="
              hover:bg-[#f0f0f0]
              py-2
              mt-3
              pl-4
              rounded-[12px]
              cursor-pointer
            "
          >
            <a href="https://www.twitter.com/kanunonso_" target="_blank">Twitter</a>
          </div>
        </div>
      </section>
    </transition>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      isNavOpen: true,
    }
  },
}
</script>
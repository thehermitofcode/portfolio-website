<template>
  <section v-if="!isNavOpen" class="font-body font-bold text-sm fixed z-50 top-0 right-0 overflow-y-auto">
      <div class="fixed inset-0 backdrop-blur-sm"></div>
    <div class="relative bg-white w-80 h-screen max-w-[calc(100% - 3rem)] p-6">
      <div class="flex justify-end">
        <div
          class="hover:bg-[#f0f0f0] p-4 w-10 h-10 rounded-full cursor-pointer" @click="isNavOpen = !isNavOpen"
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
        class="hover:bg-[#f0f0f0] py-2 mt-6 pl-4 rounded-[12px] cursor-pointer"
      >
        <p>Projects</p>
      </div>
      <div
        class="hover:bg-[#f0f0f0] py-2 mt-3 pl-4 rounded-[12px] cursor-pointer"
      >
        <p>Articles</p>
      </div>
      <div
        class="hover:bg-[#f0f0f0] py-2 mt-3 pl-4 rounded-[12px] cursor-pointer"
      >
        <p>GitHub</p>
      </div>
      <div
        class="hover:bg-[#f0f0f0] py-2 mt-3 pl-4 rounded-[12px] cursor-pointer"
      >
        <p>Twitter</p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
    data() {
        return {
            isNavOpen: false
        }
    },
    // methods: {
    //     change() {
    //         this.isNavOpen = !this.isNavOpen
    //         console.log(this.isNavOpen)
    //     }
    // }
}
</script>
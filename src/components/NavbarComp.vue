<template>
  <nav>
    <!-- Parent -->
    <div class="border-b lg:py-3">
      <div class="flex flex-col lg:flex-row justify-between">
        <!-- Brand Start -->
        <div class="flex justify-between items-center border-b lg:border-b-0 py-4 lg:py-0 px-6 lg:pr-0">
          <router-link class="font-semibold uppercase" to="/"> Cashinout </router-link>
          <button @click="isOn = !isOn" class="block lg:hidden focus:outline-none">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-5 h-5">
              <path
                :class="!isOn ? 'block' : 'hidden'"
                fill-rule="evenodd"
                d="M3 6.75A.75.75 0 013.75 6h16.5a.75.75 0 010 1.5H3.75A.75.75 0 013 6.75zM3 12a.75.75 0 01.75-.75h16.5a.75.75 0 010 1.5H3.75A.75.75 0 013 12zm0 5.25a.75.75 0 01.75-.75h16.5a.75.75 0 010 1.5H3.75a.75.75 0 01-.75-.75z"
                clip-rule="evenodd"
              />
              <path
                :class="isOn ? 'block' : 'hidden'"
                fill-rule="evenodd"
                d="M5.47 5.47a.75.75 0 011.06 0L12 10.94l5.47-5.47a.75.75 0 111.06 1.06L13.06 12l5.47 5.47a.75.75 0 11-1.06 1.06L12 13.06l-5.47 5.47a.75.75 0 01-1.06-1.06L10.94 12 5.47 6.53a.75.75 0 010-1.06z"
                clip-rule="evenodd"
              />
            </svg>
          </button>
        </div>
        <!-- Brand End -->
        <!-- Menu Start -->
        <div :class="isOn ? 'block' : 'hidden'" class="py-4 lg:py-0 lg:flex flex-col lg:flex-row justify-between lg:items-center w-full px-6">
          <div class="flex flex-col lg:flex-row lg:items-center">
            <router-link :class="className" to="/about">About</router-link>
          </div>
          <!-- <div class="flex items-center">
            <router-link :class="className" to="/login">Govinda Kharisma Dewa</router-link>
            <router-link :class="className" to="/register">Logout</router-link>
          </div> -->
          <div class="flex flex-col lg:flex-row lg:items-center">
            <router-link :class="className" to="/login">Login</router-link>
            <router-link :class="className" to="/register">Register</router-link>
          </div>
        </div>
        <!-- Menu End -->
      </div>
    </div>
    <!-- Parent -->
  </nav>
</template>

<script>
import { ref } from "vue";
export default {
  name: "NavbarComp",
  setup() {
    const className = "px-4 py-2";
    const isOn = ref(false);
    return { className, isOn };
  },
};
</script>

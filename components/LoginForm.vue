<script setup>
import { ref } from 'vue';

const passwordVisible = ref(false);
function togglePasswordVisibility() {
  passwordVisible.value = !passwordVisible.value;
}
</script>
<template>
  <div class="bg-white rounded-3xl p-5 sm:p-7 xl:p-16 m-3 sm:m-0">
    <NuxtImg src="/assets/images/svg/form-logo.svg" alt="logo" class="w-[320px] h-[160px] lg:w-[360px] lg:h-[182px]" />
    <p class="text-xl font-bold text-black pt-6">Schön, dich wiederzusehen</p>
    <form action="" class="pt-6">
      <p class="text-[11px] text-[#4A4A4A] ps-2">Login</p>
      <input required type="email" placeholder="Email or phone number"
        class="w-full py-[11px] px-4 text-base font-medium text-black placeholder:text-[#ADADAE] bg-[#f5f5f5] border border-[#DEDEDE] rounded-3xl mt-1">
      <p class="text-[11px] text-[#4A4A4A] ps-2 pt-4">Password</p>
      <div class="relative">
        <input required :type="passwordVisible ? 'text' : 'password'" placeholder="Email password"
          class="w-full py-[11px] px-4 text-base font-medium text-black placeholder:text-[#ADADAE] bg-[#f5f5f5] border border-[#DEDEDE] rounded-3xl mt-1">
        <span @click="togglePasswordVisibility">
          <NuxtImg :src="passwordVisible ? '/assets/images/svg/open-eye.svg' : '/assets/images/svg/close-eye.svg'"
            alt="eye-icon" class="w-[22px] h-[15px] absolute top-[20px] end-[18px] cursor-pointer" />
        </span>
      </div>
      <div class="flex items-center justify-between pt-5">
        <div class="flex">
          <label class="switch relative inline-block w-[40px] h-[20px]">
            <input type="checkbox" class="opacity-0 w-0 h-0">
            <span
              class="slider round rounded-[34px] before:rounded-[50%] absolute top-0 left-0 right-0 bottom-0 cursor-pointer bg-[#f5f5f5] border-[0.5px] border-[#dedede] transition-[0.4s] before:absolute before:h-[14px] before:w-[14px] before:left-[2px] before:bg-white before:top-[13.6%] before:transition-all before:duration-300 before:ease-in-out"></span>
          </label>
          <p class="text-xs text-[#191919] ps-2 pt-[2px] text-nowrap tracking-[0.3px]">Remember me</p>
        </div>
        <p class="text-xs text-[#EC6707] cursor-pointer">Forgot password?</p>
      </div>
      <button
        class="text-xl font-medium text-[#4A4A4A] bg-[#DEDEDE] rounded-3xl py-[8.5px] w-full mt-6 transition-all duration-300 ease-in-out hover:text-[#EC6707] border-[2px] border-transparent hover:border-[#EC6707] hover:bg-white">Log
        in</button>
    </form>
  </div>
</template>
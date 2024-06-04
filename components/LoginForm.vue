<template>
  <div class="bg-white rounded-3xl p-16">
    <NuxtImg src="/assets/images/svg/form-logo.svg" alt="logo" class="w-[360px] h-[182px]" />
    <p class="text-xl font-bold text-black pt-6">Schön, dich wiederzusehen</p>
    <form action="" class="pt-6">
      <p class="text-[11px] text-[#4A4A4A] ps-2">Login</p>
      <input type="email" placeholder="Email or phone number"
        class="w-full py-[11px] px-4 text-base font-medium text-black placeholder:text-[#ADADAE] bg-[#f5f5f5] border border-[#DEDEDE] rounded-3xl mt-1">
      <p class="text-[11px] text-[#4A4A4A] ps-2 pt-4">Password</p>
      <input type="password" placeholder="Email password"
        class="w-full py-[11px] px-4 text-base font-medium text-black placeholder:text-[#ADADAE] bg-[#f5f5f5] border border-[#DEDEDE] rounded-3xl mt-1 relative">
        <div class="flex items-center justify-between pt-5">
      <label class="switch">
        <input type="checkbox">
        <span class="slider round"></span>
      </label>
      <p class="text-xs text-[#EC6707]">Forgot password?</p>
      </div>
      <button
        class="text-xl font-medium text-[#4A4A4A] bg-[#DEDEDE] rounded-3xl py-[8.5px] w-full mt-6 transition-all duration-300 ease-in-out hover:text-[#EC6707] border-[2px] border-transparent hover:border-[#EC6707] hover:bg-white">Log
        in</button>
    </form>
  </div>
</template>
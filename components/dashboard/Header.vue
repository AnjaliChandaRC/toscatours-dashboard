<template>
    <div class="h-[104px] bg-white py-[19px] px-12 flex justify-between">
        <div class="hidden lg:block">
            <h2 class="text-2xl font-bold text-black">Hi Stéphane</h2>
            <p class="text-base font-medium text-[#4A4A4A] pt-2">Lass uns heute den Umsatz überprüfen!</p>
        </div>
        <div class="flex items-center">
            <NuxtImg src="/assets/images/svg/message-icon.svg" alt="message-icon"
                class="w-[20px] h-[20px] cursor-pointer" />
            <NuxtImg src="/assets/images/svg/notification-icon.svg" alt="notification-icon"
                class="w-[24px] h-[24px] mx-10 cursor-pointer" />
            <div class="flex items-center cursor-pointer">
                <NuxtImg src="/assets/images/svg/profile-icon.svg" alt="profile-icon"
                    class="w-[48px] h-[48px] me-4" />
                <div>
                    <h3 class="text-base font-bold text-black">Stéphane</h3>
                    <p class="text-[11px] text-[#4A4A4A] pt-1">Geschäftsführer</p>
                </div>
            </div>
        </div>
    </div>
</template>
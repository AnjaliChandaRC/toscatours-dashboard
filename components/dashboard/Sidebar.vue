<script setup>
// import { ref } from 'vue';

import SidebarAngeboteIcon from '../common/icons/SidebarAngeboteIcon.vue';
import SidebarBuchungenIcon from '../common/icons/SidebarBuchungenIcon.vue';
import SidebarDashboardIcon from '../common/icons/SidebarDashboardIcon.vue';
import SidebarKundenIcon from '../common/icons/SidebarKundenIcon.vue';
// import DashboardCards from './DashboardCards.vue';
// import DashboardGraph from './DashboardGraph.vue';
// import DashboardComponents from './DashboardComponents.vue';

const sidebarList = [
    {
        title: "Dashboard",
        icon: SidebarDashboardIcon,
        // component: DashboardComponents,
    },
    {
        title: "Kunden",
        icon: SidebarKundenIcon,
        // component: DashboardGraph,
    },
    {
        title: "Angebote",
        icon: SidebarAngeboteIcon,
        // component: DashboardCards,
    },
    {
        title: "Buchungen",
        icon: SidebarBuchungenIcon,
        // component: DashboardGraph,
    },
];
// const activeComponent = ref(null);

// const handleSidebarItemClick = (component) => {
//     activeComponent.value = component;
// };
</script>

<template>
    <div class="flex">
        <div class="w-[256px] bg-white min-h-screen pt-6 pb-10 flex justify-between flex-col">
            <div>
                <NuxtLink to="/">
                    <NuxtImg src="/assets/images/svg/form-logo.svg" alt="logo"
                        class="w-[200px] h-[101px] ms-6 me-[29px] mb-2" />
                </NuxtLink>
                <div v-for="(obj, index) in sidebarList" :key="index" class="pt-4">
                    <!-- @click="handleSidebarItemClick(obj.component)" -->
                    <div
                        class="ps-8 group cursor-pointer hover:bg-[#FEF8F3] flex justify-between items-center sidebar_links">
                        <div class="flex">
                            <component :is="obj.icon" class="w-5 h-5 me-2" />
                            <p class="text-sm font-medium text-black group-hover:text-[#EC6707]">{{ obj.title }}</p>
                        </div>
                        <div class="group-hover:bg-[#EC6707] bg-transparent w-[4px] h-[48px] rounded-lg"></div>
                    </div>
                </div>
            </div>
            <div
                class="mx-[33px] px-[10px] py-[28px] bg-[#f5f5f5] text-center rounded-xl border border-dotted border-[#DEDEDE]">
                <NuxtImg src="/assets/images/svg/sidebar-plus.svg" alt="sidebar-plus"
                    class="w-[39px] h-[39px] mx-auto" />
                <p class="text-[13px] font-semibold text-black pt-2">Daten importieren</p>
                <p class="text-[9px] font-medium pt-1"><span class="text-[#EC6707] underline">Datei aussuchen</span>
                    <span class="text-[#ADADAE]">oder
                        hierher
                        ziehen.</span>
                </p>
            </div>
        </div>
        <div>
            <component v-if="activeComponent" :is="activeComponent" />
        </div>
    </div>
</template>

<style scoped>
.group:hover svg path {
    fill: #EC6707;
}
</style>
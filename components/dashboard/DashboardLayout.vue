<script setup lang="ts">
import Sidebar from './Sidebar.vue';
import Header from './Header.vue';
import DashboardCards from './DashboardCards.vue';
import DashboardGraph from './DashboardGraph.vue';
import DashboardOffers from './DashboardOffers.vue';
</script>

<template>
    <div class="flex bg-[#f5f5f5]">
        <Sidebar />
        <div>
            <Header />
            <div>
                <DashboardCards />
            </div>
            <div class="flex">
                <DashboardGraph />
                <DashboardOffers />
            </div>
        </div>
    </div>
</template>
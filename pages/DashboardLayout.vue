<script setup lang="ts">
</script>

<template>
    <div class="flex bg-[#f5f5f5]">
        <DashboardSidebar />
        <div class="w-full">
            <DashboardHeader />
            <div class="px-12">
                <DashboardCards />
            </div>
            <div class="flex px-12 gap-8">
                <DashboardGraph />
                <DashboardOffers />
            </div>
        </div>
    </div>
</template>
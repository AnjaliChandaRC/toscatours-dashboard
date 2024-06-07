<script setup>
import CardsGreenArrow from '../common/icons/CardsGreenArrow.vue';
import CardsIconOne from '../common/icons/CardsIconOne.vue';
import CardsIconThree from '../common/icons/CardsIconThree.vue';
import CardsIconTwo from '../common/icons/CardsIconTwo.vue';
import CardsRedArrow from '../common/icons/CardsRedArrow.vue';

const cardsList = [
    {
        title: "166,580 CHF",
        subTitle: "Umsatz",
        decs: "5%",
        decs2: "im letzten Monat",
        icon: CardsIconOne,
        icon2: CardsGreenArrow,
    },
    {
        title: "567",
        subTitle: "Buchungen",
        decs: "2%",
        decs2: "im letzten Monat",
        icon: CardsIconTwo,
        icon2: CardsGreenArrow,
    },
    {
        title: "801",
        subTitle: "Kunden",
        decs: "3%",
        decs2: "im letzten Monat",
        icon: CardsIconThree,
        icon2: CardsRedArrow,
    },
];
</script>

<template>
    <div class="flex justify-between gap-5 flex-wrap pt-14 mt-1 pb-8">
        <div class="bg-white rounded-3xl p-6 w-[48%] xl:w-[250px] min-[1400px]:w-[340px] hover:shadow-[0px_0px_10px_#FF3B30] transition-all duration-300 ease-in-out"
            v-for="(obj, index) in cardsList" :key="index">
            <div class="flex">
                <component :is="obj.icon" class="w-6 h-6 me-2" />
                <p class="text-base text-black">{{ obj.subTitle }}</p>
            </div>
            <p class="text-[32px] font-medium text-black py-2">{{ obj.title }}</p>
            <div class="flex items-center">
                <component :is="obj.icon2" class="w-4 h-4 me-[6px]" />
                <p :class="['text-base', 'font-medium', index === 2 ? 'text-[#FF3B30]' : 'text-[#26A212]']">{{ obj.decs
                    }}</p>
                <p class="text-base font-medium text-[#ADADAE] ps-1">{{ obj.decs2 }}</p>
            </div>
        </div>
    </div>
</template>
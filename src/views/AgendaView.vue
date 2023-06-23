<template>
  <div class="relative py-16">
    <div
      ref="fbDecorativeLink"
      class="fixed z-30 hidden transition-opacity duration-300 md:block bottom-6 left-6"
    >
      <StylingFBLink></StylingFBLink>
    </div>

    <div class="fixed bottom-32 md:bottom-[57px] right-2 sm:right-1 md:right-[72px] z-10">
      <MoveToTop></MoveToTop>
    </div>
    <a href="#"
      ><div class="logoTxt hidden md:block w-[250px] h-[125px] bg-cover fixed left-0 top-2"></div
    ></a>

    <div class="flex flex-col items-center mt-12 mb-16 md:mt-0">
      <StylingTitle>
        <template #default>
          <span>議程資訊</span>
        </template>
      </StylingTitle>
    </div>

    <div class="w-[500px] mx-auto">
      <div class="flex">
        <AgendaDateHeading isActive>
          <p class="text-center">8/11 (FRI.)</p>
        </AgendaDateHeading>
        <AgendaDateHeading isRight>
          <p class="text-center">8/12 (FRI.)</p>
        </AgendaDateHeading>
      </div>
      <div class="pt-2 flex ext-custom-teal-500 border-x border-custom-teal-500">
        <div class="basis-2/12 t">cc</div>
        <div class="basis-10/12 flex gap-2">
          <div class="basis-1/3 bg-custom-pink-700">dd</div>
          <div class="basis-1/3 bg-custom-pink-700">dd</div>
          <div class="basis-1/3 bg-custom-pink-700">dd</div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.titleDecoration {
  background: url("@/assets/images/title_display.svg") no-repeat;
}

.fbIcon {
  background-image: url("@/assets/images/icon/ic_fb_l.svg");
}

.logoTxt {
  background-image: url("@/assets/images/logo_windows_txt.png");
}

.writing-vertical {
  writing-mode: vertical-rl;
}
</style>

<script setup>
import { onMounted, ref } from "vue";
import { useRoute } from "vue-router";
import { usePageInfoStore } from "@/stores/pageInfo";
import StylingTitle from "@/components/StylingTitle.vue";
import StylingFBLink from "@/components/StylingFBLink.vue";
import MoveToTop from "@/components/moveToTop.vue";
import AgendaDateHeading from "@/components/AgendaDateHeading.vue";

const route = useRoute();

const pageInfoStore = usePageInfoStore();
const { setCurrentPageName } = pageInfoStore;

const fbDecorativeLink = ref();

const scrollHandler = () => {
  const { scrollTop } = document.documentElement;
  const clientHeight = document.documentElement.clientHeight - 470;
  const isBottom = scrollTop > clientHeight;

  fbDecorativeLink.value.style.opacity = isBottom ? 0 : 1;
};

onMounted(() => {
  setCurrentPageName(route.name);
  window.addEventListener("scroll", scrollHandler);
});
</script>

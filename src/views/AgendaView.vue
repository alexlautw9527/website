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

    <div class="w-full mx-auto px-[140px] relative">
      <div class="flex">
        <AgendaDateHeading isActive>
          <p class="text-center">8/11 (FRI.)</p>
        </AgendaDateHeading>
        <AgendaDateHeading isRight>
          <p class="text-center">8/12 (FRI.)</p>
        </AgendaDateHeading>
      </div>
      <div class="p-2 flex flex-col border border-custom-teal-500 gap-2 border">
        <div class="flex gap-2">
          <div class="basis-[10%]"></div>
          <div class="basis-[90%] flex gap-2">
            <div class="basis-1/3 bg-custom-pink-700 py-5 text-center">講廳 1001</div>
            <div class="basis-1/3 bg-custom-pink-700 py-5 text-center">講廳 1002</div>
            <div class="basis-1/3 bg-custom-pink-700 py-5 text-center">講廳 1003</div>
          </div>
        </div>

        <div class="flex min-h-[186px] gap-2">
          <div
            class="py-5 basis-[10%] text-custom-teal-500 flex flex-col justify-between items-center"
          >
            <p>09:00</p>
            <div class="grow flex items-center items-center">
              <div class="border-l border-custom-teal-500 h-1/2"></div>
            </div>
            <p>09:50</p>
          </div>
          <div class="basis-[90%] flex gap-2">
            <div class="basis-1/3 border border-custom-teal-500"></div>
            <div class="basis-1/3 border border-custom-teal-500"></div>
            <div class="basis-1/3 border border-custom-teal-500"></div>
          </div>
        </div>

        <!-- 休息時間元件 -->
        <div class="flex gap-2">
          <div class="basis-[10%] gap-2"></div>
          <div class="basis-[90%] flex text-custom-teal-500 justify-center py-4">
            {{ "休息時間" }}
          </div>
        </div>

        <!-- 一般情況元件 -->
        <div class="flex min-h-[186px] gap-2">
          <div
            class="py-5 basis-[10%] text-custom-teal-500 flex flex-col justify-between items-center"
          >
            <p>09:00</p>
            <div class="grow flex items-center">
              <div class="border-l border-custom-teal-500 h-1/2"></div>
            </div>
            <p>09:50</p>
          </div>
          <div class="basis-[90%] flex gap-2">
            <div class="basis-1/3 border border-custom-teal-500 px-5 py-4">
              <SpeakerCell></SpeakerCell>
            </div>
            <div class="basis-1/3 border border-custom-teal-500"></div>
            <div class="basis-1/3 border border-custom-teal-500"></div>
          </div>
        </div>

        <!-- 一般情況元件 -->
        <div class="flex min-h-[186px] gap-2">
          <div
            class="py-5 basis-[10%] text-custom-teal-500 flex flex-col justify-between items-center"
          >
            <p>09:00</p>
            <div class="grow flex items-center">
              <div class="border-l border-custom-teal-500 h-1/2"></div>
            </div>
            <p>09:50</p>
          </div>
          <div class="basis-[90%] flex gap-2">
            <div class="basis-1/3 border border-custom-teal-500 px-5 py-4">
              <SpeakerCell></SpeakerCell>
            </div>
            <div class="basis-1/3 border border-custom-teal-500"></div>
            <div class="basis-1/3 border border-custom-teal-500"></div>
          </div>
        </div>

        <!-- 一般情況元件 -->
        <div class="flex min-h-[186px] gap-2">
          <div
            class="py-5 basis-[10%] text-custom-teal-500 flex flex-col justify-between items-center"
          >
            <p>09:00</p>
            <div class="grow flex items-center">
              <div class="border-l border-custom-teal-500 h-1/2"></div>
            </div>
            <p>09:50</p>
          </div>
          <div class="basis-[90%] flex gap-2">
            <div class="basis-1/3 border border-custom-teal-500 px-5 py-4">
              <SpeakerCell></SpeakerCell>
            </div>
            <div class="basis-1/3 border border-custom-teal-500"></div>
            <div class="basis-1/3 border border-custom-teal-500"></div>
          </div>
        </div>

        <!-- keynote 元件 -->
        <div class="flex min-h-[186px] gap-2">
          <div
            class="py-5 basis-[10%] text-custom-teal-500 flex flex-col justify-between items-center"
          >
            <p>09:00</p>
            <div class="grow flex items-center">
              <div class="border-l border-custom-teal-500 h-1/2"></div>
            </div>
            <p>09:50</p>
          </div>
          <div class="basis-[90%] flex border border-custom-teal-500 items-center">
            <div class="h-full basis-1/3 px-5 py-4">
              <SpeakerCell></SpeakerCell>
            </div>
            <div
              class="h-[90%] text-lg basis-1/3 border-l border-custom-teal-700 text-custom-teal-500 flex items-center justify-center"
            >
              同步投影
            </div>
            <div
              class="h-[90%] text-lg basis-1/3 border-l border-custom-teal-700 text-custom-teal-500 flex items-center justify-center"
            >
              同步投影
            </div>
          </div>
        </div>

        <div class="flex gap-2">
          <div class="basis-[10%] gap-2"></div>
          <div class="basis-[90%] flex text-custom-teal-500 justify-center py-4">明天見</div>
        </div>
      </div>

      <!-- 靜態 Footer -->
      <div class="border border-custom-teal-500 border-t-0 flex gap-2 p-2" ref="staticFooterRef">
        <div class="basis-[10%] flex">
          <div class="text-lg grow bg-custom-teal-500 text-black flex items-center justify-center">
            8/11
          </div>
          <div
            class="text-lg grow border border-custom-teal-700 text-custom-teal-700 flex justify-center items-center"
          >
            8/12
          </div>
        </div>
        <div class="basis-[90%] flex gap-2">
          <div class="basis-1/3 bg-custom-pink-700 py-3 text-center">講廳 1001</div>
          <div class="basis-1/3 bg-custom-pink-700 py-3 text-center">講廳 1002</div>
          <div class="basis-1/3 bg-custom-pink-700 py-3 text-center">講廳 1003</div>
        </div>
      </div>

      <!-- 吸底元件 -->
      <div
        class="footer right-0 left-0 px-[140px]"
        :class="{
          'footer-visible': isVisible,
          'footer-animated-hidden': !isVisible,
          hidden: isHideDynamicFooter,
        }"
      >
        <div class="p-2 flex gap-2 border border-custom-teal-500 bg-black">
          <div class="basis-[10%] flex">
            <div
              class="text-lg grow bg-custom-teal-500 text-black flex items-center justify-center"
            >
              8/11
            </div>
            <div
              class="text-lg grow border border-custom-teal-700 text-custom-teal-700 flex justify-center items-center"
            >
              8/12
            </div>
          </div>
          <div class="basis-[90%] flex gap-2">
            <div class="basis-1/3 bg-custom-pink-700 py-3 text-center">講廳 1001</div>
            <div class="basis-1/3 bg-custom-pink-700 py-3 text-center">講廳 1002</div>
            <div class="basis-1/3 bg-custom-pink-700 py-3 text-center">講廳 1003</div>
          </div>
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

.footer {
  transition: all 0.5s ease;
  position: fixed;
  width: inherit;
  bottom: 0;
}

.footer-animated-hidden {
  transform: translateY(100%);
}

.footer-visible {
  transform: translateY(0%);
}
</style>

<script setup>
import { onMounted, onBeforeUnmount, ref, watch } from "vue";
import { useRoute } from "vue-router";
import { usePageInfoStore } from "@/stores/pageInfo";
import StylingTitle from "@/components/StylingTitle.vue";
import StylingFBLink from "@/components/StylingFBLink.vue";
import MoveToTop from "@/components/MoveToTop.vue";
import AgendaDateHeading from "@/components/agenda/AgendaDateHeading.vue";
import SpeakerCell from "@/components/agenda/SpeakerCell.vue";

const route = useRoute();

const pageInfoStore = usePageInfoStore();
const { setCurrentPageName } = pageInfoStore;

const fbDecorativeLink = ref();

const handleFBScroll = () => {
  const { scrollTop } = document.documentElement;
  const clientHeight = document.documentElement.clientHeight - 470;
  const isBottom = scrollTop > clientHeight;

  fbDecorativeLink.value.style.opacity = isBottom ? 0 : 1;
};

const isVisible = ref(false);

watch(isVisible, (value) => {
  if (value) {
    console.log(isVisible.value);
  }
});

const isHideDynamicFooter = ref(false);
const isStaticFooterVisible = ref(false);

const lastScrollTop = ref(0);

const handleFooterScroll = () => {
  if (isHideDynamicFooter.value) {
    return;
  }

  const st = window.pageYOffset || document.documentElement.scrollTop;
  if (st > lastScrollTop.value) {
    isVisible.value = true;
  }

  if (!isStaticFooterVisible.value && st < lastScrollTop.value) {
    isVisible.value = false;
  }

  if (isStaticFooterVisible.value && st < lastScrollTop.value) {
    isVisible.value = true;
  }

  lastScrollTop.value = st;
};

let scrollDownObserver = null;
let isStaticFooterObserver = null;

const staticFooterRef = ref(null);

onBeforeUnmount(() => {
  window.removeEventListener("scroll", handleFooterScroll, false);

  if (scrollDownObserver) {
    scrollDownObserver.disconnect();
  }
});

onMounted(() => {
  window.addEventListener("scroll", handleFooterScroll, false);

  setCurrentPageName(route.name);
  window.addEventListener("scroll", handleFBScroll);

  scrollDownObserver = new IntersectionObserver(
    ([entry]) => {
      isHideDynamicFooter.value = entry.isIntersecting;
    },
    {
      threshold: 1,
    }
  );

  scrollDownObserver.observe(staticFooterRef.value);

  isStaticFooterObserver = new IntersectionObserver(
    ([entry]) => {
      isStaticFooterVisible.value = entry.isIntersecting;
    },
    {
      threshold: 0,
    }
  );

  isStaticFooterObserver.observe(staticFooterRef.value);
});
</script>

<template>
<!--  <ConfigProvider>-->
<!--    <router-view/>-->
<!--  </ConfigProvider>-->

  <div class="mt-[100px] h-full" style="border: 1px solid beige">
    <PteIntroduce />
  </div>
</template>

<script setup>
import {onMounted, reactive} from 'vue';
import {useRouter, RouterView} from 'vue-router';
import {getMenuData, clearMenuItem} from '@ant-design-vue/pro-layout';
import ContactView from "./views/contacts/ContactView.vue";
import ContactResult from "./views/contacts/ContactResult.vue";
import PteIntroduce from "./views/introduces/PteIntroduce.vue";

const locale = (i18n) => i18n;
const router = useRouter();

const {menuData} = getMenuData(clearMenuItem(router.getRoutes()));

const state = reactive({
  collapsed: false, // default value
  openKeys: ['/dashboard'],
  selectedKeys: ['/welcome'],
})
const layoutConf = reactive({
  navTheme: 'dark',
  layout: 'mix',
  splitMenus: false,
  menuData,
});

onMounted(() => {
});

</script>
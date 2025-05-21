<script setup>
// import Link from "#imports";
const route = useRoute();
</script>
<template>
    <header class="app">
        <section class="logo">
            <NuxtImg
                src="/assets/imgs/logo.png"
                format="png"
                alt="لوگو سایت"
                :width="70"
                :height="39"
            />
        </section>
        <section class="left">
            <NuxtLink
                :href="route.fullPath.split('/')[1] == 'add' ? '#' : '/add'"
                :class="{ active: route.fullPath.split('/')[1] == 'add' }"
            >
                ثبت آدرس
            </NuxtLink>
            <NuxtLink
                :href="route.fullPath.split('/')[1].length == 0 ? '#' : '/'"
                :class="{ active: route.fullPath.split('/')[1].length == 0 }"
                >مشاهده آدرس ها
            </NuxtLink>
        </section>
    </header>
</template>
<style lang="scss" scoped>
header.app {
    position: fixed;
    top: 0;
    left: 0;
    padding: 20px 100px;
    width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    box-shadow:
        0 1px 3px 0 rgb(0 0 0 / 0.1),
        0 1px 2px -1px rgb(0 0 0 / 0.1);
    background: #f7f7f7;
    box-sizing: border-box;
    transition: all linear 0.2s;
}
header.app section.left {
    column-gap: 20px;
    display: flex;
    flex-direction: row;
    align-items: center;
    transition: all linear 0.2s;
}
header.app section.left a {
    padding: 0 15px;
    font-family: Vazir;
    font-size: 14px;
    font-weight: bold;
    color: var(--primary-color);
}
header.app section.left a.active {
    color: var(--text-color);
}
@media only screen and (max-width: 600px) {
    header.app {
        padding: 20px;
    }
}
@media only screen and (max-width: 410px) {
    header.app section.left {
        column-gap: 0px;
    }
}
</style>

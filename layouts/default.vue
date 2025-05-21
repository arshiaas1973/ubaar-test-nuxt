<script setup>
useHead({
    htmlAttrs: { dir: "rtl", lang: "fa" },
    bodyAttrs: { style: "margin:0 !important; padding: 0 !important" },
});
</script>
<template>
    <AppHeader />
    <main>
        <slot />
    </main>
</template>
<style lang="scss" scoped>
main {
    margin: 105px auto 0 auto;
    max-width: 800px;
}
</style>

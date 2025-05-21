<script setup>
const Step = ref(1);
</script>
<template>
    <section class="main">
        <h2 class="title">
            <Icon
                name="material-symbols:arrow-right-alt-rounded"
                style="font-weight: 100"
                :size="25"
            />
            <span> انتخاب آدرس </span>
        </h2>
        <div class="info">
            <h2>لطفا مشخصات و آدرس خود را وارد کنید</h2>
            <div class="form"></div>
        </div>
    </section>
</template>
<style lang="scss">
section.main {
}
section.main .title {
    display: flex;
    flex-direction: row;
    column-gap: 20px;
    align-items: center;
    color: var(--text-color);
    font-family: Vazir;
}
section.main .title {
    font-size: 16px;
    line-height: 32px;
}
section.main div.info {
    background: #f7f7f7;
    padding: 10px 50px;
    border-radius: 6px;
    box-shadow:
        0 4px 6px -1px rgb(0 0 0 / 0.1),
        0 2px 10px 2px rgb(0 0 0 / 0.1);
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    row-gap: 30px;
}
section.main div.info h2 {
    font-family: Vazir;
    font-size: 16px;
    font-weight: bold;
    line-height: 32px;
    color: var(--text-color);
    margin: 0;
}
section.main div.info div.form {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    column-gap: 30px;
}
</style>

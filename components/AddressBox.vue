<script setup>
defineProps({
    firstName: "",
    lastName: "",
    phoneNumber: "",
    telNumber: "",
    gender: "",
    address: "",
});
</script>
<template>
    <div class="box">
        <div>
            <span>نام</span>
            <h2>{{ firstName }}</h2>
        </div>
        <div>
            <span>نام خانوادگی</span>
            <h2>{{ lastName }}</h2>
        </div>
        <div>
            <span>شماره تلفن همراه</span>
            <h2>{{ phoneNumber }}</h2>
        </div>
        <div>
            <span>شماره تلفن ثابت</span>
            <h2>{{ telNumber }}</h2>
        </div>
        <div>
            <span>جنسیت</span>
            <h2>{{ gender }}</h2>
        </div>
        <hr />
        <div>
            <span>آدرس</span>
            <h2>{{ address }}</h2>
        </div>
    </div>
</template>
<style lang="scss" scoped>
div.box {
    background: #f7f7f7;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    padding: 30px;
    row-gap: 30px;
    column-gap: 10px;
    box-sizing: border-box;
    border-radius: 6px;
    box-shadow:
        0 4px 6px -1px rgb(0 0 0 / 0.1),
        0 2px 10px 2px rgb(0 0 0 / 0.1);
    transition: all linear 0.2s;
}
div.box div {
    display: flex;
    flex-direction: column;
    flex-basis: calc(1 / 3 * (100% - 2 * 10px));
    row-gap: 5px;
    font-family: Vazir;
    transition: all linear 0.2s;
}
div.box div h2 {
    font-size: 16px;
    font-weight: bold;
    display: -webkit-box;
    display: -moz-box;
    overflow: hidden;
    line-clamp: 1;
    -webkit-line-clamp: 1;
    -webkit-box-orient: vertical;
    word-wrap: anywhere;
    text-wrap: wrap;
    transition: all linear 0.2s;
}
div.box div span {
    font-size: 14px;
    font-weight: bold;
    color: #9b9b9b;
}
div.box hr {
    display: none;
    height: 3px;
    border-radius: 1px;
    margin-left: 0;
    margin-right: 0;
    background: #ededed;
    flex-basis: calc(100% - 2 * 10px);
    border: 0;
}
@media only screen and (max-width: 640px) {
    div.box div {
        flex-basis: calc(1 / 2 * (100% - 2 * 10px));
    }
}
@media only screen and (max-width: 440px) {
    div.box div {
        flex-basis: calc(100% - 2 * 10px);
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
    }
    div.box hr {
        display: block;
    }
    div.box {
        row-gap: 20px;
    }
    div.box div:last-of-type {
        /* margin-top: -15px; */
        flex-direction: column;
        justify-content: inherit;
        align-items: inherit;
    }
    div.box div h2 {
        margin: 0;
    }
    div.box div:last-of-type h2 {
        display: block;
        overflow: hidden;
        line-clamp: none;
        -webkit-line-clamp: none;
    }
}
</style>

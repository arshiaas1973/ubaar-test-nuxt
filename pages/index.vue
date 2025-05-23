<template>
    <main>
        <h2 class="title">آدرس ها و مشخصات</h2>
        <div class="adresses">
            <AddressBox
                firstName="علی"
                address="لورتمیسنتمنسیتنمتشسنمتنیمتشسمنکتکینسشتنمتیسشنمتیسشنتنسیش نیمتشس شیستیشس منتیشس منتیشس تنمیشستن تیشسنمتیشس تنمشس"
                lastName="خریدار"
                gender="مرد"
                phoneNumber="09123456790"
                telNumber="0123456790"
            />
        </div>
    </main>
</template>
<style lang="scss" scoped>
main {
    background: transparent;
    color: var(--text-color);
    display: flex;
    flex-direction: column;
    padding: 0 30px;
}
main h2.title {
    margin: 10px 0;
    font-family: Vazir;
    font-size: 16px;
    font-weight: 400;
    line-height: 32px;
}
main div.adresses {
    display: flex;
    flex-direction: column;
    row-gap: 20px;
}
</style>

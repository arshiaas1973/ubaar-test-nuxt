<template>
    <main>
        <h2 class="title">آدرس ها و مشخصات</h2>
        <AddressBox
            firstName="علی"
            address="لورتمیسنتمنسیتنمتشسنمتنیمتشسمنکتکینسشتنمتیسشنمتیسشنتنسیش نیمتشس شیستیشس منتیشس منتیشس تنمیشستن تیشسنمتیشس تنمشس"
            lastName="خریدار"
            gender="مرد"
            phoneNumber="09123456790"
            telNumber="0123456790"
        />
    </main>
</template>
<style lang="scss" scoped>
main {
    margin: 105px auto 0 auto;
    max-width: 800px;
    background: transparent;
    color: var(--text-color);
    display: flex;
    flex-direction: column;
    row-gap: 20px;
    padding: 0 30px;
}
main h2.title {
    font-family: Vasir;
    font-size: 16px;
    font-weight: 400;
    line-height: 32px;
}
</style>

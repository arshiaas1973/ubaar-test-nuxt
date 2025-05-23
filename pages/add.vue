<script setup>
const Step = ref(1);
const Name = ref("");
const LastName = ref("");
const PhoneNumber = ref("");
const TelNumber = ref("");
const Address = ref("");
const Gender = ref("");
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
        <Transition name="slide-fade" :duration="200">
            <div class="info">
                <h2>لطفا مشخصات و آدرس خود را وارد کنید</h2>
                <div class="form">
                    <section>
                        <span>نام</span>
                        <div class="field">
                            <input
                                type="text"
                                v-model="Name"
                                required
                                placeholder="مثل: علی"
                            />
                            <button
                                :class="{ showed: Name.length > 0 }"
                                @click="
                                    () => {
                                        Name = '';
                                    }
                                "
                            >
                                <Icon
                                    name="material-symbols:cancel"
                                    class="icon"
                                    :size="18"
                                />
                            </button>
                        </div>
                    </section>
                    <section>
                        <span>نام خانوادگی</span>
                        <div class="field">
                            <input
                                type="text"
                                v-model="LastName"
                                required
                                placeholder="مثل: رضایی"
                            />
                            <button
                                :class="{ showed: LastName.length > 0 }"
                                @click="
                                    () => {
                                        LastName = '';
                                    }
                                "
                            >
                                <Icon
                                    name="material-symbols:cancel"
                                    class="icon"
                                    :size="18"
                                />
                            </button>
                        </div>
                    </section>
                    <section>
                        <span>شماره تلفن همراه</span>
                        <div class="field">
                            <input
                                v-model="PhoneNumber"
                                required
                                placeholder="مثل: 09123456789"
                                type="text"
                                maxlength="11"
                            />
                            <button
                                :class="{ showed: PhoneNumber.length > 0 }"
                                @click="
                                    () => {
                                        PhoneNumber = '';
                                    }
                                "
                            >
                                <Icon
                                    name="material-symbols:cancel"
                                    class="icon"
                                    :size="18"
                                />
                            </button>
                        </div>
                    </section>
                    <section>
                        <span
                            style="
                                display: flex;
                                flex-direction: row;
                                justify-content: space-between;
                                align-items: center;
                                row-gap: 0;
                            "
                        >
                            <span>
                                شماره تلفن ثابت
                                <span style="font-size: 12px"> (اختیاری) </span>
                            </span>
                            <span style="font-size: 11px; color: #9d9d9d">
                                با پیش شماره
                            </span>
                        </span>
                        <div class="field">
                            <input
                                v-model="TelNumber"
                                placeholder="مثل: 02123456789"
                                type="tel"
                                maxlength="11"
                            />
                            <button
                                :class="{ showed: TelNumber.length > 0 }"
                                @click="
                                    () => {
                                        TelNumber = '';
                                    }
                                "
                            >
                                <Icon
                                    name="material-symbols:cancel"
                                    class="icon"
                                    :size="18"
                                />
                            </button>
                        </div>
                    </section>
                    <section style="flex-grow: 1">
                        <span> آدرس </span>
                        <div class="field">
                            <input
                                v-model="Address"
                                required
                                type="text"
                                minlength="10"
                            />
                            <button
                                :class="{ showed: Address.length > 0 }"
                                @click="
                                    () => {
                                        Address = '';
                                    }
                                "
                            >
                                <Icon
                                    name="material-symbols:cancel"
                                    class="icon"
                                    :size="18"
                                />
                            </button>
                        </div>
                    </section>
                </div>
                <div class="gender">
                    <span> جنسیت: </span>
                    <div>
                        <section>
                            <label for="woman"> خانم </label>
                            <input
                                type="radio"
                                id="woman"
                                v-model="Gender"
                                value="خانم"
                            />
                        </section>
                        <section>
                            <label for="man"> آقا </label>
                            <input
                                type="radio"
                                id="man"
                                v-model="Gender"
                                value="آقا"
                            />
                        </section>
                    </div>
                </div>
            </div>
        </Transition>
    </section>
    <footer></footer>
</template>
<style lang="scss" scoped>
.slide-fade-enter-active {
    transition: all 0.3s ease-out;
}

.slide-fade-leave-active {
    transition: all 0.8s cubic-bezier(1, 0.5, 0.8, 1);
}

.slide-fade-enter-from,
.slide-fade-leave-to {
    transform: translateX(calc(1 / 3 * 100%));
    opacity: 0;
}
section.main .title {
    display: flex;
    flex-direction: row;
    column-gap: 20px;
    align-items: center;
    color: var(--text-color);
    font-family: Vazir;
    font-size: 16px;
    line-height: 32px;
    font-weight: 400;
    margin: 10px 0;
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
    row-gap: 30px;
}
section.main div.info div.form section {
    display: flex;
    flex-direction: column;
    row-gap: 5px;
    box-sizing: border-box;
    flex-basis: calc(1 / 3 * (100% - 60px));
}
section.main div.info div.form section span,
section.main div.info div.gender span,
section.main div.info div.gender div label {
    font-family: Vazir;
    font-size: 14px;
    line-height: 28px;
    font-weight: 500;
    color: var(--text-color);
}
section.main div.info div.form section div.field {
    display: inline-flex;
    flex-direction: row;
    align-items: center;
}
section.main div.info div.form section div.field button {
    background: transparent;
    padding: 0;
    margin: 0;
    border: 0;
    outline: none;
    display: flex;
    justify-content: center;
    align-items: center;
    /* height: calc(100% + 10px); */
    margin-right: -27px;
}
section.main div.info div.form section div.field button .icon {
    color: var(--text-color);
    opacity: 0;
    cursor: pointer;
    transition: all linear 0.2s;
}
section.main div.info div.form section div.field button.showed .icon {
    opacity: 0.5;
}
section.main div.info div.form section div.field button.showed .icon:hover {
    opacity: 0.8;
}
section.main div.info div.form section div.field input {
    padding: 10px 10px 10px 30px;
    border-radius: 3px;
    font-family: Vazir;
    font-size: 14px;
    font-weight: 500;
    border: 0;
    outline: 2px solid #d9d9d9;
    transition: all linear 0.2s;
    background: transparent;
    width: 100%;
    caret-color: var(--primary-color);
    caret-shape: bar;
    direction: rtl;
}
section.main div.info div.form section div.field input:focus {
    outline: 2px solid var(--primary-color);
}
section.main div.info div.gender {
    display: flex;
    flex-direction: row;
    max-width: 300px;
    justify-content: space-between;
    margin-bottom: 30px;
}
section.main div.info div.gender div {
    display: flex;
    flex-direction: row;
    column-gap: 30px;
}
section.main div.info div.gender div input {
    font-family: Vazir;
    font-size: 14px;
    font-weight: 500;
    accent-color: var(--primary-color);
    cursor: pointer;
}
footer {
    position: fixed;
    display: flex;
    bottom: 0;
    left: 0;
    padding: 20px 0;
    box-shadow:
        0 1px 3px 0 rgb(0 0 0 / 0.1),
        0 1px 2px -1px rgb(0 0 0 / 0.1);
    background: #f7f7f7;
}
</style>

<template>
    <div>
        <footer class="footer__bottom center">
            <div class="Interno">
                <h2 class="footer__bottom__header"><img src="../assets/header_logo.svg" alt="logo">Interno</h2>
                <p class="footer__bottom__text">It is a long established fact that a reader will be distractedv
                    lookings.</p>
            </div>
            <div class="pages">
                <h2 class="pages__contacts__header">Pages</h2>
                <router-link class="pages__contacts__text" to="/">Home</router-link>
                <router-link class="pages__contacts__text" to="/Project">Project</router-link>
                <router-link class="pages__contacts__text" to="/Blog">Blog</router-link>
            </div>
            <div class="contacts">
                <h2 class="pages__contacts__header">Contacts</h2>
                <p class="pages__contacts__text">55 East Birchwood Ave. Brooklyn, New York 11201 contact@interno.com (123)
                    456 - 7890</p>
            </div>

        </footer>

    </div>
</template>

<script>
export default {
    name: 'FooterComp',

    data() {
        return {

        };
    },

    mounted() {

    },

    methods: {

    },
};
</script>

<style lang="scss" scoped>
.center {
    padding-left: calc(50% - 570px);
    padding-right: calc(50% - 570px);
}

.footer__bottom {
    display: flex;
    align-items: flex-start;
    gap: 210px;
    padding-top: 96px;

    &__header {
        color: #292F36;
        font-family: "DM Serif Display";
        font-size: 40px;
        font-style: normal;
        font-weight: 400;
        line-height: 125%;
        /* 50px */
    }
}

.pages {
    display: flex;
    flex-direction: column;
    color: #292F36;


}

.pages__contacts__header {
    color: #292F36;

    font-family: "DM Serif Display";
    font-size: 25px;
    font-style: normal;
    font-weight: 600;
    line-height: 125%;
}

.footer__bottom__text {
    color: #4D5053;
    font-family: Jost;
    font-size: 22px;
    font-style: normal;
    font-weight: 400;
    line-height: 150%;
    /* 33px */
    letter-spacing: 0.22px;
}

.pages__contacts__text {
    color: #4D5053;
    font-family: Jost;
    font-size: 22px;
    font-style: normal;
    font-weight: 400;
    line-height: 300%;
    /* 66px */
    letter-spacing: 0.22px;
}

@media (max-width: 1024px) {
    .center {
        padding-left: calc(50% - 376px);
        padding-right: calc(50% - 376px);
    }
}

@media (max-width: 767px) {
    .center {
        padding-left: 16px;
        padding-right: 16px;
    }

    .footer__bottom {
        display: flex;
        align-items: flex-start;
        gap: 40px;
        padding-top: 96px;
    }
}

@media (max-width: 420px) {
    .footer__bottom {
        display: flex;
        align-items: flex-start;
        gap: 20px;
        padding-top: 50px;
        flex-direction: column;
    }
}
</style>
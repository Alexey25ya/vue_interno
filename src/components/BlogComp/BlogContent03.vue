<template>
    <div>
        <div class="blog__cards">
            <div class="design__card" v-for="{ id, img, text, header, date, arrow } in cards" :key="id">
                <img class="design__img" :src="img" alt="design">
                <p class="design__text">{{ text }}</p>
                <h2 class="design__card__header">{{ header }}</h2>
                <div class="design__card__bottom">
                    <p class="design__card__date">{{ date }}</p>
                    <router-link class="pages__contacts__text" to="/blog-details"><img :src="arrow"
                            alt="arrow"></router-link>
                </div>
            </div>

        </div>
    </div>
</template>

<script>
export default {
    name: 'BlogContent01',

    data() {
        return {
            cards: [
                {
                    id: 1,
                    img: require('../../assets/design2.png'),
                    text: 'Kitchan Design',
                    header: 'Let’s Get Solution For Building Construction Work',
                    date: '26 December,2022',
                    arrow: require('../../assets/arrow.svg'),
                },
                {
                    id: 2,
                    img: require('../../assets/design1.png'),
                    text: 'Kitchan Design',
                    header: 'Let’s Get Solution For Building Construction Work',
                    date: '26 December,2022',
                    arrow: require('../../assets/arrow.svg'),
                },
                {
                    id: 3,
                    img: require('../../assets/design5.png'),
                    text: 'Kitchan Design',
                    header: 'Let’s Get Solution For Building Construction Work',
                    date: '26 December,2022',
                    arrow: require('../../assets/arrow.svg'),
                },
                {
                    id: 4,
                    img: require('../../assets/design4.png'),
                    text: 'Kitchan Design',
                    header: 'Let’s Get Solution For Building Construction Work',
                    date: '26 December,2022',
                    arrow: require('../../assets/arrow.svg'),
                },
                // {
                //     id: 5,
                //     img: require('../../assets/design3.png'),
                //     text: 'Kitchan Design',
                //     header: 'Let’s Get Solution For Building Construction Work',
                //     date: '26 December,2022',
                //     arrow: require('../../assets/arrow.svg'),
                // },
                // {
                //     id: 6,
                //     img: require('../../assets/design3.png'),
                //     text: 'Kitchan Design',
                //     header: 'Let’s Get Solution For Building Construction Work',
                //     date: '26 December,2022',
                //     arrow: require('../../assets/arrow.svg'),
                // }
            ]


        };
    },

    mounted() {

    },

    methods: {

    },
};
</script>

<style lang="scss" scoped>
.blog__cards {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
}

.design__card {
    position: relative;
    border-radius: 50px;

    &__header {
        width: 270px;
        color: #292F36;
        font-family: "DM Serif Display";
        font-size: 25px;
        font-style: normal;
        font-weight: 400;
        line-height: 125%;
        /* 31.25px */
        letter-spacing: 0.5px;
    }

    &__bottom {
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
}

.design__img {
    border-top-right-radius: 50px;
    border-top-left-radius: 50px;
}

.design__text {
    position: absolute;
    top: 50%;
    left: 10%;
    border-radius: 8px 8px 8px 0px;
    background: #FFF;
}

@media (max-width: 1024px) {
    .center {
        padding-left: calc(50% - 376px);
        padding-right: calc(50% - 376px);
    }

    .blog__mid__content__header {
        display: flex;
        justify-content: center;
    }

    .blog__mid__content__box {
        display: flex;
        align-items: center;
        gap: 65px;
        flex-direction: column;
    }
}

@media (max-width: 767px) {
    .center {
        padding-left: 16px;
        padding-right: 16px;
    }

    .blog__mid__content__box {
        &__img {
            width: 100%;
            border-radius: 50px;
        }
    }

    .blog__bottom__content__header {
        display: flex;
        justify-content: center;
    }

    .blog__cards {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .design__card__bottom {
        display: flex;
        align-items: center;
        gap: 150px;
    }
}
</style>
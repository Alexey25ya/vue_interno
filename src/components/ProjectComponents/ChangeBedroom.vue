<template>
    <div>
        <div class="design__cards center">
            <div class="design__card" v-for="{ id, img, text, header, date, arrow } in cards" :key="id">
                <img class="design__img" :src="img" alt="design">
                <div class="design__card__content">
                    <div class="design__card__content__discription">
                        <p class="design__text">{{ text }}</p>
                        <h2 class="design__card__header">{{ header }}</h2>
                        <p class="design__card__date">{{ date }}</p>
                    </div>
                    <router-link class="pages__contacts__text" to="/project-details"><img :src="arrow"
                            alt="arrow"></router-link>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ChangeBedroom',

    data() {
        return {
            cards: [
                {
                    id: 1,
                    img: require('../../assets/bedroom1.png'),
                    text: 'Bedroom Design',
                    header: 'Let’s Get Solution For Building Construction Work',
                    date: '26 December,2022',
                    arrow: require('../../assets/arrow.svg'),
                },
                {
                    id: 2,
                    img: require('../../assets/bedroom2.png'),
                    text: 'Bedroom Design',
                    header: 'Let’s Get Solution For Building Construction Work',
                    date: '26 December,2022',
                    arrow: require('../../assets/arrow.svg'),
                },
                {
                    id: 3,
                    img: require('../../assets/bedroom3.png'),
                    text: 'Bedroom Design',
                    header: 'Let’s Get Solution For Building Construction Work',
                    date: '26 December,2022',
                    arrow: require('../../assets/arrow.svg'),
                },
                {
                    id: 4,
                    img: require('../../assets/bedroom4.png'),
                    text: 'Bedroom Design',
                    header: 'Let’s Get Solution For Building Construction Work',
                    date: '26 December,2022',
                    arrow: require('../../assets/arrow.svg'),
                },
                {
                    id: 5,
                    img: require('../../assets/bedroom5.png'),
                    text: 'Bedroom Design',
                    header: 'Let’s Get Solution For Building Construction Work',
                    date: '26 December,2022',
                    arrow: require('../../assets/arrow.svg'),
                },
                {
                    id: 6,
                    img: require('../../assets/bedroom6.png'),
                    text: 'Bedroom Design',
                    header: 'Let’s Get Solution For Building Construction Work',
                    date: '26 December,2022',
                    arrow: require('../../assets/arrow.svg'),
                }]

        };
    },

    mounted() {

    },

    methods: {

    },
};
</script>

<style lang="scss" scoped>
.design__cards {
    display: grid;
    grid-template-columns: repeat(2, 600px);
    padding: 48px;
    justify-content: center;
    align-items: center;
}

.design__card {
    display: flex;
    flex-direction: column;
    padding-left: 30px;

    &__content {
        display: flex;
        align-items: center;
    }
}

@media (max-width: 1024px) {
    .center {
        padding-left: calc(50% - 376px);
        padding-right: calc(50% - 376px);
    }

    .design__cards {
        display: flex;
        flex-direction: column;
        gap: 30px;
    }
}

@media (max-width: 767px) {
    .center {
        padding-left: 16px;
        padding-right: 16px;
    }
}
</style>
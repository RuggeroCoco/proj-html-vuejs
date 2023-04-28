<script>
export default {
    data() {
        return {
            subTitle: 'ABOUT THE NETWORK',
            title: {
                highlight: 'The',
                end: 'Company'
            },
            description: 'For 12 years we have been providing audit and warranty, financial advice, risk advice, taxes and related services to select clients.',
            cards: [
                { icon: 'fa-medal', title: 'Tradition', description: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.' },
                { icon: 'fa-lock', title: 'Security', description: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.' },
                { icon: 'fa-pen-to-square', title: 'Certificate', description: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.' },
                { icon: 'fa-graduation-cap', title: 'Expertise', description: 'Lorem ipsum dolor sit amet consectetur adipiscing elit.' },
            ]
        }
    }
}
</script>

<template>
    <div class="company d-flex">
        <div class="section info">
            <div class="title">
                <p class="fw-bold about">{{ subTitle }}</p>
                <h3 class="fs-1 fw-bold"><span class="the">{{ title.highlight }}</span> {{ title.end }}</h3>
            </div>
            <div class="text-left">
                <p class="text-secondary">{{ description }}</p>
            </div>
            <div class="cards">
                <div class="card" v-for="card in cards" :key="card.title">
                    <div>
                        <i :class="'fa-solid me-2 ' + card.icon"></i><span class="fs-4 fw-bold">{{ card.title }}</span>
                    </div>
                    <p class="text-secondary">{{ card.description }}</p>
                </div>
            </div>
        </div>
        <div class="section">
            <img src="../assets/images/about-3.jpg" alt="" class="photo">
        </div>
    </div>
</template>

<style scoped lang="scss">
.company {
    width: 100%;

    .section {
        width: 50%;

    }

    .info {
        padding: 8rem 2rem 5rem 10rem;

        i {
            color: #038483;
        }
    }

    .about {
        color: #39c4c6;
    }

    .the {
        color: #038483;
        background-color: rgba($color: #038483, $alpha: 0.1);
        padding: .2rem .7rem;
        border-radius: .5rem;
    }

    .cards {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        grid-gap: 2rem;
    }

    .card {
        border: none;
    }

    section {
        width: 50%;
    }


    .photo {
        max-width: 100%;
        max-height: 100%;
    }

    .card {
        div {
            display: flex;
            align-items: center;
        }
    }

}
</style>
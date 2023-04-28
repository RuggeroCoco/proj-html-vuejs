<script>
export default {
    data() {
        return {
            subtitle: "OUR BUSINESS AREAS",
            title: {
                start: "Excellence in",
                higtlight: "Services",
            },
            description: "We are leaders in providing consultancy services with a set of cutting-edge technologies and a team of experienced and renowned professionals. These are some options that you can hire.",
            cards: [
                {
                    icon: "fa-network-wired", title: "Audit & Assurance", description: "Lorem ipsum dolor sit amet consectetur adipiscing elit."
                },
                {
                    icon: "fa-briefcase", title: "Financial Advisory", description: "Lorem ipsum dolor sit amet consectetur adipiscing elit."
                },
                {
                    icon: "fa-chart-simple", title: "Analytics and M&A", description: "Lorem ipsum dolor sit amet consectetur adipiscing elit."
                },
                {
                    icon: "fa-plane-up", title: "Middle Marketing", description: "Lorem ipsum dolor sit amet consectetur adipiscing elit."
                },
                {
                    icon: "fa-globe", title: "Legal Consulting", description: "Lorem ipsum dolor sit amet consectetur adipiscing elit."
                },
                {
                    icon: "fa-inbox", title: "Regulatory Risk", description: "Lorem ipsum dolor sit amet consectetur adipiscing elit."
                },
            ]
        }
    }
}
</script >

<template>
    <div class="wrapper">
        <div class="container">
            <p class="subtitle">{{ subtitle }}</p>
            <h2 class="text-white">{{ title.start }} <span class="higtlight">{{ title.higtlight }}</span> </h2>
            <div class="d-flex align-items-center justify-content-between">
                <p class="text-light me-5">{{ description }}</p>
                <input type="button" value="SEE ALL" class="button" />
            </div>
            <div class="cards pt-3">
                <div class="card" v-for="card in cards" :key="card.title">
                    <i :class="'icon fa-solid me-2 mb-3 ' + card.icon"></i>
                    <div class="fs-4 fw-bold text-white mb-2">{{ card.title }}</div>
                    <p class="text-secondary">{{ card.description }}</p>
                    <input type="button" value="READ MORE" class="button" />
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
.wrapper {
    background-color: #1e2223;
    width: 100%;

    .container {
        padding: 2rem 7rem;

        .subtitle {
            color: #39c4c6;
        }

        .higtlight {
            background-color: rgba($color: #038483, $alpha: 0.3);
            border-radius: .2rem;
            padding: .2rem .7rem;
        }

        .button {
            border: 1px solid #0d7e7e;
            color: white;
            background-color: transparent;
            border-radius: 5px;
            padding: 0.2rem 0.8rem;
            transition: all 300ms;

            &:hover {
                background-color: #0d7e7e;
            }
        }

        .cards {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            grid-gap: 2rem;
        }

        .card {
            display: flex;
            flex-direction: column;
            align-items: start;
            padding: 2rem;
            border: none;
            background-color: #4e4d51;

            .icon {
                color: #0d7e7e;
                font-size: x-large;
            }
        }
    }
}
</style>
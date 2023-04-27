<script>
export default {
    data() {
        return {
            description: 'A Functional HTML Template for Corporate & Buisiness',
            contacts: {
                phone: "+1(305) 1234-5678",
                email: "hello@example.com",
                position: "Main Avenue,987",
            },
            sections: [{
                title: 'About',
                links: [
                    {
                        label: 'The Company', url: '/'
                    },
                    { label: 'The Company', url: '/' },
                    { label: 'The Company', url: '/' },
                    { label: 'The Company', url: '/' },
                    { label: 'The Company', url: '/' },
                    { label: 'The Company', url: '/' },
                    { label: 'The Company', url: '/' }
                ]
            }, {
                title: 'About',
                links: [
                    {
                        label: 'The Company', url: '/'
                    },
                    { label: 'The Company', url: '/' },
                    { label: 'The Company', url: '/' },
                    { label: 'The Company', url: '/' },
                    { label: 'The Company', url: '/' },
                    { label: 'The Company', url: '/' },
                    { label: 'The Company', url: '/' }
                ]
            }, {
                title: 'About',
                links: [
                    {
                        label: 'The Company', url: '/'
                    },
                    { label: 'The Company', url: '/' },
                    { label: 'The Company', url: '/' },
                    { label: 'The Company', url: '/' },
                    { label: 'The Company', url: '/' },
                    { label: 'The Company', url: '/' },
                    { label: 'The Company', url: '/' }
                ]
            }]
        }
    }
};
</script>

<template>
    <div class="footer">
        <div class="footer-content">
            <div class="footer-main">
                <img src="../assets/images/logo.png">
                <p>
                    {{ description }}
                </p>
                <div class="footer-contacts">
                    <div>
                        <i class="fa-solid fa-phone me-2"></i>
                        <a>{{ contacts.phone }}</a>
                    </div>
                    <div>
                        <i class="fa-solid fa-envelope me-2"></i>
                        <a>{{ contacts.email }}</a>
                    </div>
                    <div>
                        <i class="fa-solid fa-location-dot me-2"></i>
                        <a>{{ contacts.position }}</a>
                    </div>
                </div>
                <input type="input" class="button" value="GET IN TOUCH" />
            </div>
            <div class="footer-sections d-flex">
                <div class="section" v-for="(section, index) in sections" :key="index">
                    <h5 class="title">{{ section.title }}</h5>
                    <div class="section-link d-flex align-items-center justify-content-center" v-for="link in section.links"
                        :key="link.label">
                        <i class="fa-solid fa-chevron-right me-2 d-flex align-items-center"></i>
                        <a :href="link.url" class="pb-1">{{ link.label }}</a>
                    </div>
                </div>
            </div>
        </div>
        <div class="footer-bottom">
            <div class="footer-bottom-content">
                <p>
                    Enjoy the low price. We are tracking any intention of privacy
                </p>
                <p>
                    © NEXGEN is Proudly Powered by <span>Codings</span>
                </p>
            </div>

        </div>
    </div>
</template>



<style scoped lang="scss">
.footer {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background-color: #1e2223;

    &-content {
        padding: 3rem 0;
        max-width: 80%;
        font-size: 0.8rem;
        display: flex;
    }

    &-main {
        color: #e3e7df;
        max-width: 25%;
    }


    &-contacts {
        margin-bottom: 1rem;

        div {
            margin-bottom: 0.5rem;
        }
    }


    &-sections {
        margin-left: 3rem;

        .section {
            background-color: #4e4d51;
            padding: 2.5rem 3rem;
            border-radius: 8px;

            .title {
                color: white;
                margin-bottom: 1rem;
            }

            &-link {
                a {
                    text-decoration: none;
                    color: #e3e7df
                }
            }

            &:not(:last-child) {
                margin-right: 1.5rem;
            }
        }
    }

    &-bottom {
        margin-top: 2rem;
        padding: 1.5rem 0;
        width: 100%;
        background-color: #121117;

        &-content {
            padding: 0 12rem;
            display: flex;
            justify-content: space-between;

            p {
                span {
                    color: #0d7e7e;
                }
            }
        }

    }

    .button {
        text-align: center;
        border: 1px solid #0d7e7e;
        color: white;
        background-color: transparent;
        border-radius: 5px;
        padding: 0.2rem 0.8rem;
        transition: all 300ms;
        cursor: pointer;

        &:hover {
            background-color: #0d7e7e;
        }
    }

}
</style>
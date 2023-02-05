<template>
    <section id="bottom-navigation" class="block fixed inset-x-0 bottom-0 z-10 rounded-t-lg shadow-inner navbar">
        <div id="tabs" class="flex justify-between">

            <NuxtLink :to="link.goto" v-for="link in Links"
                class="w-full focus:text-black focus:font-extrabold hover:text-teal-500 justify-center inline-block text-center pt-2 pb-1">
                <img class="inline-block mb-1" :src="link.imageSource" alt="image" />
                <span class="tab tab-home block">{{ link.navTitle }}</span>
            </NuxtLink>
            <div
                class="w-full focus:text-black focus:font-extrabold justify-center inline-block text-center pt-2 pb-1">
                <img class="inline-block mb-1" src="~/assets/dark-mode.png" alt="image" />
                <select v-model="$colorMode.preference">
                    <option value="light" class="tab tab-home block">Light Mode</option>
                    <option value="dark" class="tab tab-home block">Dark Mode</option>
                </select>
            </div>



        </div>
    </section>
</template>

<script>
import homeIcon from '~/assets/home.png'
import scanQRIcon from '~/assets/qr-code.png'
import historyIcon from '~/assets/history.png'
const colorMode = useColorMode()

export default {

    data() {
        return {
            Links: [
                {
                    'id': 1,
                    'imageSource': homeIcon,
                    'navTitle': "Home",
                    'goto': "/"
                },
                {
                    'id': 2,
                    'imageSource': scanQRIcon,
                    'navTitle': "Scan QR",
                    'goto': "scanqr"
                },
                {
                    'id': 3,
                    'imageSource': historyIcon,
                    'navTitle': "History",
                    'goto': "history"
                },

            ],
            colors: ['system', 'light', 'dark', 'sepia'],
            'themeTitle': "Dark Mode"
        }
    },
    methods: {

    },
    mounted() {

    }
}

</script>
<style>
.dark-mode body {
    background-color: #091a28;
    color: #ebf4f1;
}

.dark-mode .navbar {
    background-color: #091a28;
    color: #ebf4f1;
}

.light-mode body {
    background-color: #fff;
    color: rgba(0, 0, 0, 0.8);
}

.light-mode .navbar {
    background-color: #fff;
    color: rgba(0, 0, 0, 0.8);
}
</style>


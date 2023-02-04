<template>
    <section id="bottom-navigation" class="block fixed inset-x-0 bottom-0 z-10 rounded-t-lg shadow-inner bg-zinc-300">
        <div id="tabs" class="flex justify-between">
           
                <NuxtLink :to="link.goto" v-for="link in Links"
                class="w-full focus:text-black focus:font-extrabold hover:text-teal-500 justify-center inline-block text-center pt-2 pb-1">
                <img class="inline-block mb-1" :src="link.imageSource" alt="image" />
                <span class="tab tab-home block text-xs">{{ link.navTitle }}</span>
            </NuxtLink>
           

        </div>
    </section>
</template>

<script>
import homeIcon from '~/assets/home.png'
import scanQRIcon from '~/assets/qr-code.png'
import historyIcon from '~/assets/history.png'
import darkModeIcon from '~/assets/dark-mode.png'


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
                {
                    'id': 4,
                    'imageSource': darkModeIcon,
                    'navTitle': "Dark Mode",
                    'goto': "thememode"
                },
            ],
        }
    }
}

</script>


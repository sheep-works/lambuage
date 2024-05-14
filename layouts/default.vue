<template>
    <v-app>
        <v-layout class="rounded rounded-md">

            <v-app-bar :elevation="2" style="position: fixed; top:0; z-index: 100; width: 100%">

                <template v-slot:title>
                    <HomeIcon />
                </template>
                <v-spacer></v-spacer>
                <v-item-group id="nav-items" class="mr-10">
                    <v-item>
                        <v-btn outlined>
                            <a href="/#">トップ</a>
                        </v-btn>
                    </v-item>
                    <v-item>
                        <v-btn outlined>
                            <a href="/#contents">業務内容</a>
                        </v-btn>
                    </v-item>
                    <v-item>
                        <v-btn>
                            <a href="/#information">会社概要</a>
                        </v-btn>
                    </v-item>
                    <v-item>
                        <v-btn>
                            <a href="/#inquire">お問い合わせ</a>
                        </v-btn>
                    </v-item>
                    <v-item>
                        <v-btn>
                            <NuxtLink to="news">お知らせ</NuxtLink>
                        </v-btn>
                    </v-item>
                </v-item-group>

            </v-app-bar>
            <!-- <v-navigation-drawer location="end">
                <v-list>
                    <v-list-item title="Navigation drawer"></v-list-item>
                </v-list>
            </v-navigation-drawer> -->

            <v-main class="d-flex align-center justify-center" style="min-height: 300px;">
                <slot />
            </v-main>
            <v-footer app name="footer" border>
                <v-container fluid class="text-center">
                    Copyright © 2024- Lambuage LLC. All rights reserved
                </v-container>

            </v-footer>
        </v-layout>
    </v-app>
</template>

<script setup lang="ts">
import HomeIcon from '~/components/HomeIcon.vue';
// useHead({
//     script: [
//         {
//             src: "https://www.googletagmanager.com/gtag/js?id=G-PFT0GHJFSL",
//             async: 'true'
//         },
//         {
//             type: "text/javascript",
//             innerHTML: "window.dataLayer = window.dataLayer || [];function gtag(){dataLayer.push(arguments);};gtag('js', new Date());gtag('config', 'G-PFT0GHJFSL');"
//         }
//     ],
// });
</script>

<style>
#nav-items a {
    color: inherit;
    font-size: larger;
    text-decoration: none;
}

#nav-items a:visited {
    color: inherit;
}
</style>
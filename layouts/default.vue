<template>
    <v-app>
        <v-layout class="rounded rounded-md">

            <v-app-bar :elevation="2">

                <template v-slot:title>
                    <HomeIcon />
                </template>

            </v-app-bar>
            <!-- <v-navigation-drawer location="end">
                <v-list>
                    <v-list-item title="Navigation drawer"></v-list-item>
                </v-list>
            </v-navigation-drawer> -->

            <v-main class="d-flex align-center justify-center" style="min-height: 300px; width: 1000px;">
                <slot />
            </v-main>
            <v-footer app name="footer" color="blue-grey-lighten-2">
                <v-btn class="mx-auto" variant="text">
                    Get data
                </v-btn>
            </v-footer>
        </v-layout>
    </v-app>
</template>
  
<script setup lang="ts">
import type HomeIconVue from '~/components/HomeIcon.vue';
import HomeIcon from '~/components/HomeIcon.vue';
</script>
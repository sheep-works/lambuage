<template>
    <v-container fluid>
        <v-card class="pa-6" elevation="5">
            <v-card-title :class="position === 'left' ? 'text-right' : 'text-left'">

            </v-card-title>
            <v-card-text>
                <v-row v-if="position === 'left'">
                    <v-col>
                        <v-parallax :src="src" height="500" />
                    </v-col>
                    <v-col flex-column class="text-center">
                        <h2 class="text-h4 font-weight-bold mb-4">
                            {{ title }}
                        </h2>
                        <div class="text-body-1">
                            <slot />
                        </div>
                    </v-col>
                </v-row>
                <v-row v-else>
                    <v-col flex-column class="text-center">
                        <h2 class="text-h4 font-weight-bold mb-4">
                            {{ title }}
                        </h2>
                        <div class="text-body-1">
                            <slot />
                        </div>
                    </v-col>
                    <v-col>
                        <v-parallax :src="src" height="500" />
                    </v-col>
                </v-row>
            </v-card-text>
            <v-card-actions v-if="link !== undefined">
                <a :href="link.href" target="_blank">{{ link.text }}</a>
            </v-card-actions>
        </v-card>
    </v-container>
</template>

<script setup lang="ts">
interface Props {
    position: "right" | "left"
    src: string
    title: string
    link?: {
        text: string
        href: string
    }
}
const props = defineProps<Props>()
</script>
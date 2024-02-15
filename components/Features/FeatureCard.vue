<template>
    <section>
        <v-card class="pa-6" elevation="5">
            <v-card-title :class="position === 'left' ? 'text-right' : 'text-left'">

            </v-card-title>
            <v-card-text>
                <v-row v-if="position === 'left'">
                    <v-col cols="12" md="5">
                        <v-parallax :src="src" height="500" />
                    </v-col>
                    <v-col class="text-center">
                        <h2 class="text-h4 font-weight-bold mb-4">
                            {{ title }}
                        </h2>
                        <div class="text-body-1">
                            <slot />
                            <v-sheet v-if="link !== undefined" class="my-4">
                                <a :href="link.href" target="_blank">{{ link.text }}</a>
                            </v-sheet>
                        </div>
                    </v-col>
                </v-row>
                <v-row v-else>
                    <v-col class="text-center" cols="12" md="7" order="1" order-md="1" order-sm="2" order-xs="2"
                        order-lg="1">
                        <h2 class="text-h4 font-weight-bold mb-4">
                            {{ title }}
                        </h2>
                        <div class="text-body-1">
                            <slot />
                            <v-sheet v-if="link !== undefined">
                                <a :href="link.href" target="_blank">{{ link.text }}</a>
                            </v-sheet>
                        </div>
                    </v-col>
                    <v-col order-md="1">
                        <v-parallax :src="src" height="500" />
                    </v-col>
                </v-row>
            </v-card-text>

        </v-card>
    </section>
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
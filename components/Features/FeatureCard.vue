<template>
    <v-container fluid class="ma-6">
        <v-card class="pa-6">
            <v-card-title :class="position === 'left' ? 'text-right' : 'text-left'">

            </v-card-title>
            <v-card-text>
                <v-row v-if="position === 'left'">
                    <v-col>
                        <v-parallax :src="src" />
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
                        <v-parallax :src="src" />
                    </v-col>

                </v-row>
            </v-card-text>
        </v-card>
    </v-container>
</template>

<script setup lang="ts">
interface Props {
    position: "right" | "left"
    src: string
    title: string
}
const props = defineProps<Props>()
</script>
<template>
    <v-app>
        <navigation></navigation>
        <v-content>
            <v-container>
                <v-layout row>
                    <v-flex xs12>
                        <v-card>
                            <v-card-title>Production & Consommation</v-card-title>
                            <v-card-text>
                                <radial-apex-chart></radial-apex-chart>
                            </v-card-text>
                        </v-card>
                    </v-flex>
                </v-layout>
                <v-layout row class="mt-4">
                    <v-flex xs12>
                        <v-card>
                            <v-card-title>Energie soutir + inject + autoconsommation</v-card-title>
                            <v-card-text>
                                <stacked-area-apex-chart></stacked-area-apex-chart>
                            </v-card-text>
                        </v-card>
                    </v-flex>
                </v-layout>
                <v-layout row class="mt-4">
                    <v-flex xs9 class="mr-4">
                        <conseils></conseils>
                    </v-flex>
                    <v-flex xs3>
                        <linky></linky>
                    </v-flex>
                </v-layout>
            </v-container>
        </v-content>
    </v-app>
</template>

<script>
    import Navigation from '../components/Navigation.vue'
    import RadialApexChart from '../components/RadialApexChart.vue'
    import StackedAreaApexChart from '../components/StackedAreaApexChart.vue'
    import Conseils from '../components/Conseils.vue'
    import Linky from '../components/Linky.vue'

    export default {
        name: 'App',
        components: {
            Navigation,
            RadialApexChart,
            StackedAreaApexChart,
            Conseils,
            Linky
        },
        data() {
            return {}
        }
    }
</script>

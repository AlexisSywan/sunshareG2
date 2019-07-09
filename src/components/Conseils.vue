<template>
    <v-card>
        <v-card-title>Des conseils, des économies</v-card-title>
        <v-card-text>
            <v-list>
                <v-list-tile v-for="(conseil, c) in conseils" :key="c" @click="">
                    <v-list-tile-content>
                        <v-list-tile-title v-html="conseil.title"></v-list-tile-title>
                        <v-divider></v-divider>
                    </v-list-tile-content>
                </v-list-tile>
            </v-list>
        </v-card-text>
    </v-card>
</template>

<script>
    export default {
        name: "Conseils",
        data() {
            return {
                conseils: [
                    {title: "On adopte le réflexe « heures creuses »"},
                    {title: "On choisit les bons appareils électroménagers"},
                    {title: "On entretient notre réfrigérateur régulièrement"},
                    {title: "On évite de laisser les appareils en veille"},
                    {title: "On préfère la douche au bain"},
                    {title: "On remplace les ampoules incandescentes par des ampoules LED"},
                    {title: "On modifie nos habitudes pour cuisiner"},
                    {title: "On évite de surchauffer notre logement"},
                    {title: "On optimise la climatisation de notre logement"},
                ]
            }
        }
    }
</script>

<style scoped>

</style>

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
                    {title: "Les consommations éléctriques"},
                    {title: "Le multimédia"},
                    {title: "Le lavage"},
                    {title: "Le froid"},
                    {title: "Le petit éléctroménager"},
                    {title: "L'éclairage"},
                    {title: "La cuisson"},
                ]
            }
        }
    }
</script>

<style scoped>

</style>

<template>
    <v-card>
        <v-card-title>Informations Linky</v-card-title>
        <v-card-text class="text-xs-center">
            <p>{{linkyValue}}</p>
        </v-card-text>
    </v-card>
</template>

<script>
    export default {
        name: "Linky",
        data() {
            return {
                linkyValue: '233454 KWH BASE'
            }
        }
    }
</script>

<style scoped>

</style>

<template>
    <v-toolbar dark color="#0187866e">
        <v-toolbar-title>
            <v-img :src="logo" width="80px"></v-img>
        </v-toolbar-title>

        <v-spacer></v-spacer>

        <v-toolbar-title>
            Admin
        </v-toolbar-title>
    </v-toolbar>
</template>

<script>
    export default {
        name: "Navigation",
        data() {
            return {
                logo: require('@/assets/images/sunshare.png')
            }
        }
    }
</script>

<style scoped>

</style>

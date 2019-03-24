<template>
    <v-toolbar>
        <v-img src="./Logo.svg" content position height="70%"></v-img>
        <v-spacer></v-spacer>
        <div class="hidden-sm-and-down text-uppercase">
            <v-btn flat>About</v-btn>
            <v-btn flat class="">Post Your Project</v-btn>
            <v-btn flat class="secondary">Login</v-btn>
            <v-btn flat class="primary">Create an account</v-btn>
        </div>
        </v-toolbar>
</template>
<script type="text/javascript">
export default {
    data() {
        return {

        }
    }
}
</script>
<style>
.navsidebar {
    height: 100%;
    width: 30px;
    background-color: #1B264F;
    margin: 0px 24px 0px 0px;
}

.v-toolbar,.v-img {}

.v-toolbar__content,.v-toolbar__extension {
    padding: 0px 24px 0px 0px;
}
</style>
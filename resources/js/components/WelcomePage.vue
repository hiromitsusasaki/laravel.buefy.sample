<template>
    <section class="section">
        <div class="container">
            <h1 class="h1">Welcome</h1>
        </div>
        <div class="container">
            <b-field label="please put your name">
                <b-input v-model="name"></b-input>
            </b-field>
            <b-button @click="clicked">Click me</b-button>
        </div>
    </section>
</template>
<script>
export default {
    data() {
        return {
            name: "",
        }
    },
    methods: {
        clicked() {
            this.$buefy.notification.open({
                message: 'Hi ' + this.name + '. Nice to meet you!!',
                })
        }
    }
}
</script>

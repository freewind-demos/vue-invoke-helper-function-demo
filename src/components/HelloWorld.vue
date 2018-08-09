<template>
    <div class="hello">
        {{ hello(msg) }}
    </div>
</template>

<script lang="ts">
    import {Component, Prop, Vue} from 'vue-property-decorator';

    @Component
    export default class HelloWorld extends Vue {
        @Prop() private msg: string = "Vue!";

        hello(msg: string): string {
            return "Hello, " + msg;
        }
    }
</script>

<style scoped>
    .hello {
        color: red;
    }
</style>

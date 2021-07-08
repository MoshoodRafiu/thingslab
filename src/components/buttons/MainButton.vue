<template>
    <component
        :is="tag"
        :type="type"
        :disabled="disableButton"
        :href="to"
        class="main-button"
        :class="{'outline': outline}">
        <slot/>
    </component>
</template>

<script>
export default {
    name: "MainButton",
    props: {
        tag: {
            type: String,
            default: "button"
        },
        disabled: {
            type: Boolean,
            default: false
        },
        type: {
            type: String,
            default: ""
        },
        outline: {
            type: Boolean,
            default: true
        },
        to: {
            type: String
        }
    },
    data() {
        return {
            loading: false,
            disableButton: this.disabled
        };
    },

    methods: {
        startLoading() {
            this.loading = true;
            this.disableButton = true;
        },
        stopLoading() {
            this.loading = false;
            this.disableButton = false;
        }
    }
};
</script>

<style scoped>
    .main-button{
        text-decoration: none;
        color: #fff;
        padding: 20px 40px;
        background: #FD435A;
        border-radius: 50px;
        height: 57px;
        font-size: 18px;
        box-shadow: 0 0 0 0.25rem #f8d8dc;
    }

    .main-button.outline{
        background: #fff;
        color: #FD435A;
        box-shadow: none;
        border: 1px solid #FD435A;
    }

    .main-button:hover{
        color: #FD435A;
        border: 1px solid #FD435A;
        background: #fff;
        box-shadow: none;
        transition: linear all 0.3s;
    }

    .main-button.outline:hover{
        background: #FD435A;
        color: #fff;
        box-shadow: 0 0 0 0.25rem #f8d8dc;
        border: none;
    }
</style>
<template>
<view class="container">
    <text class="text-color-primary">{{message}}</text>
    <text-input
        class="text-color-primary"
        :style="{height: 40, borderColor: 'gray', borderWidth: 1}"
        v-model="message" />
   
    <button v-bind:title="message" v-bind:on-press="handleBtnPress"/>
  </view>
</template>

<script>
export default {
    data: function () {
        return {
            message: "Hello World"
        };

    },
    methods: {
        handleBtnPress: function () {
            alert('Btn Press');
        }
    }
};
</script>

<style>
.container {
    background-color: white;
    align-items: center;
    justify-content: center;
    flex: 1;
}

.text-color-primary {
    color: blue;
}
</style>

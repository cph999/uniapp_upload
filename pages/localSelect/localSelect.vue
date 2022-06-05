<template>
	<view><uni-data-select v-model="value" :localdata="range"
	 @change="change"></uni-data-select></view>
</template>

<script>
export default {
  data() {
    return {
      value: 0,
      range: [
        { value: 0, text: "篮球" },
        { value: 1, text: "足球" },
        { value: 2, text: "游泳" },
      ],
    };
  },
  methods: {
    change(e) {
      console.log("e:", e);
    },
  },
};
</script>

<style>
.text {
font-size: 12px;
color: #666;
margin-top: 5px;
}

.uni-px-5 {
padding-left: 10px;
padding-right: 10px;
}

.uni-pb-5 {
padding-bottom: 10px;
}
</style>

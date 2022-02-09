<template>
  <view class="index">
    <view v-if="condition1 === true">
      文案1
    </view>
    <view class="list-row">
      默认文案
    </view>
    <view v-if="condition2 === true">
      文案2
    </view>
  </view>
</template>

<script>
import './index.less'

export default {
    data () {
        return {
            condition1: false,
            condition2: false
        }
    },
    created() {
        this.init();
    },
    methods: {
        init() {
            setTimeout(() => {
                this.condition1 = true;
                this.condition2 = true;
            }, 1000);
        }
    }
}
</script>

<template>
    <transition name="slide-down">
            <div class="title-wrapper"
            v-show="ifTitleAndMenuShow">
                <div class="left">
                    <span class="icon-arrow-left2 icon"></span>
                </div>
                <div class="right">
                    <div class="icon-wrapper">
                        <span class="icon-list-numbered icon"></span>
                    </div>
                    <div class="icon-wrapper">
                        <span class="icon-menu icon"></span>
                    </div>
                    <div class="icon-wrapper">
                        <span class="icon-upload2 icon"></span>
                    </div>
                </div>
            </div>
        </transition>
</template>
<script>
export default {
    props:{
        ifTitleAndMenuShow:{
            type: Boolean,
            default: false
        }
    }
}
</script>
<style lang='scss' scoped>
/* eslint-disable */
@import '../assets/styles/global.scss';
.title-wrapper{
        position: absolute;
        top: 0;
        left: 0;
        z-index: 101;
        height: 54px;
        display: flex;
        width: 100%;
        
        background: white;
        box-shadow: 0 px2rem(8) px2rem(8) rgba(0, 0, 0, .15);
        .left{
            flex: 0 0 px2rem(60);
            @include center;
        }
        .right{
            flex: 1;
            display: flex;
            justify-content: flex-end;
            .icon-wrapper{
                flex: 0 0 px2rem(40);
                @include center;
            }
        }
    }
</style>

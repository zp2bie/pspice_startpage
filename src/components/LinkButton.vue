<script>

    export default{
        data(){
            return {
                testmessage:"test message for linkButton"
            }
        },
        props:['datas','strap_class']
    }
</script>
<template>
    <div class="list-group">
        <div v-for="item in datas" class="card text-white m-1" >
            <!-- <div class="card-header">Training</div> -->
            <div  :class="strap_class" >
                <h5 class="card-title  customdatademo"  :data-tooltip="item.desp">{{item.title}}</h5>
                <!-- <small class="card-text ">Description about what this item is about</small> -->
            </div>
        </div>
    </div>

</template>

<style>
    .customdatademo {
    position: relative ;
    }
    .customdatademo:hover::after {
    content: attr(data-tooltip) ;
    position: absolute ;
    top: -2.5em ;
    left: 2em ;
    min-width: 200px ;
    min-height: 50px ;
    border: 1px #f87b05 solid ;
    border-radius: 3px;
    padding: 6px ;
    /* color: black ; */
    background-color:#f08b2c ;
    z-index: 1 ;
    }
</style>
<template>
    <div class="boder-x" :class="twitterBorderColor">
        <div class="sticky top-0 px-4 py-3 bg-white/80 backdrop-blur-md dark:bg-dim-900/80">
            
            <h1 class="text-xl text-gray-900 font-bold ">{{props.title}}</h1>
        </div>

        <div v-if="props.loading" class=" flex justify-center items-center py-3 border-b" :class="twitterBorderColor">
            <UISpinner />
        </div>

        <div class="" v-else>
            <slot></slot>
        </div>
    </div>
</template>

<script setup>
const {twitterBorderColor} = useTailwindConfig()

const props = defineProps({
    title: {
        type:String,
        require:true
    },
    loading: {
        tpye:Boolean,
        default:false
    }

    })
 

</script>

 
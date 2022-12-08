<template>
    <div>
        <nuxt-link to="/" class="flex items-center hover:bg-gray-200 rounded-full w-min p-3  dark:hover:bg-dim-200 dark:text-white"
            :class="defaultTransition">
            <div class="w-6 h-6 ">
                <slot name="icon"></slot>
            </div>

            <div class="ml-4 text-xl hidden xl:block" :class="textClass">
                <slot name="text"></slot>
            </div>
        </nuxt-link>
    </div>
</template>

<script setup>

const { defaultTransition } = useTailwindConfig()

const props = defineProps({
    active:{
        type:Boolean,
        defalut:false
    }
})

const textClass = computed(()=> props.active ? 'font-semibold':'font-normal')
</script>

 
<template>
    <div class="m-2 border overflow-hidden rounded-xl bg-gray-50  dark:bg-dim-900" :class="twitterBorderColor">
        <div class="p-3 text-xl font-extrabold text-gray-900 border-b dark:text-white">

            <h1>{{ props.title }}</h1>
        </div>
        <slot></slot>

        <div class="p-3 text-sm text-blue-400 cursor-pointer hover:bg-gray-100 dark:hover:bg-dim-300" :class="defaultTransition" >
            Show more
        </div>

    </div>
</template>

<script setup>
const props = defineProps({
    title: {
        type: String,
        require: true
    }
})

const { twitterBorderColor, defaultTransition } = useTailwindConfig()

</script>

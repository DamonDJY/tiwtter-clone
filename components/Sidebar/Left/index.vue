<template>
    <div class=" h-screen flex flex-col">
        <div class="hover:bg-blue-50 rounded-full w-min p-2 my-2 dark:hover:bg-white/20" :class="defaultTransition">

            
            <nuxt-link to="/">
                <div class="w-8 h-8  text-s">
                    <LogoTwitter />
                </div>
            </nuxt-link>
        </div>

        <div class="mt-2 space-y-3">

<SidebarLeftTab active>
        <template v-slot:icon>
            <HomeIcon />
        </template>

        <template v-slot:text>

          Home
        </template>
      </SidebarLeftTab>

      <SidebarLeftTab>
        <template v-slot:icon>
            <HashtagIcon />
        </template>
        <template v-slot:text>
            Explore
        </template>
    </SidebarLeftTab>


    <SidebarLeftTab>
        <template v-slot:icon>
            <BellIcon />
        </template>
        <template v-slot:text>
            Notifications
        </template>
    </SidebarLeftTab>


    <SidebarLeftTab>
        <template v-slot:icon>
            <InboxIcon />
        </template>
        <template v-slot:text>
            Messages
        </template>
    </SidebarLeftTab>

    <SidebarLeftTab>
        <template v-slot:icon>
            <BookmarkIcon />
        </template>
        <template v-slot:text>
            Bookmarks
        </template>
    </SidebarLeftTab>


    <SidebarLeftTab>
        <template v-slot:icon>
            <DocumentTextIcon />
        </template>
        <template v-slot:text>
            Lists
        </template>
    </SidebarLeftTab>


    <SidebarLeftTab>
        <template v-slot:icon>
            <UserIcon />
        </template>
        <template v-slot:text>
            Profile
        </template>
    </SidebarLeftTab>

    <SidebarLeftTab>
        <template v-slot:icon>
            <CircleHorizontalIcon />
        </template>
        <template v-slot:text>
            More
        </template>
    </SidebarLeftTab>
    
</div>
    </div>
</template>

<script setup>
import { HomeIcon } from '@heroicons/vue/20/solid'
import { HashtagIcon, BellIcon, InboxIcon, BookmarkIcon, DocumentTextIcon, UserIcon,  PencilIcon, ChevronDownIcon } from '@heroicons/vue/24/outline'
import CircleHorizontalIcon from '~~/components/Logo/CircleHorizontalIcon.vue';

const { defaultTransition } = useTailwindConfig()
 

</script>

 
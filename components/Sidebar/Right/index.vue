<template>
    <div class="flex flex-col">

        <!-- preview card: whats happening -->
        <SidebarRightPreviewCard title="What's Happening">
            <SidebarRightPreviewCardItem v-for="(h,i) in whatsHappening" :key="i">

                <div>
                    <h2 class="font-bold text-gray-800 text-md dark:text-white">{{h.title}}</h2>
                    <p class="text-xs text-gray-400">{{h.count}}</p>
                </div>

            </SidebarRightPreviewCardItem>
        </SidebarRightPreviewCard>

        <!-- preview card: who to follow -->
        <SidebarRightPreviewCard title="Who to follow">
            <SidebarRightPreviewCardItem v-for="(w, i) in whoToFollowItems" :key="i">

                <div class="flex flex-row justify-between p-2 items-center">
                    <div class="flex flex-row">
                        <img class="w-10 h-10 rounded-full" :src="w.image" :alt="w.name">

                        <div class="flex flex-col ml-2">
                            <h1 class="text-sm font-bold text-gray-900 dark:text-white">{{w.name}}</h1>
                            <p class="text-xs text-gray-400">{{ w.handle }}</p>
                        </div>
                    </div>

                    <div class="flex h-full">
                        <button class="px-4 py-2 font-bold text-xs text-white dark:text-black bg-black dark:bg-white rounded-full">Follow</button>
                    </div>
                </div>

            </SidebarRightPreviewCardItem>
        </SidebarRightPreviewCard>
    </div>
</template>

<script setup>
const whoToFollowItems = ref([
    {
        name: 'Rodrigo Rahman',
        handle: '@RRahman',
        image: 'https://picsum.photos/200/200'
    },
    {
        name: 'Gustavo Guanabara',
        handle: '@GGuanabara',
        image: 'https://picsum.photos/200/200'
    },
    {
        name: 'Lucas Montano',
        handle: '@LMontano',
        image: 'https://picsum.photos/200/200'
    },
])

const whatsHappening = ref([
    {
        title: 'SpaceX',
        count: '18.8k Tweets'
    },
    {
        title: 'Flutter is Awesome',
        count: '328.4k Tweets'
    },
    {
        title: 'Nuxt is incredible',
        count: '139.3k Tweets'
    },
])
</script>

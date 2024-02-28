<script setup lang="ts">
    const items = [{
        label: 'Tag 1',
        items: [{
            label: 'Station 1',
            locationLabel: 'Wald Kirche',
            hint1: 'blablub',
            hint2: 'blaaabluuub',
            solution: 'langweilig'
        }, {
            label: 'Station 2',
            locationLabel: 'Jahnkampfbahn',
            hint1: 'blablub',
            hint2: 'blaaabluuub',
            solution: 'langweilig'
        }]
    }, {
        label: 'Tag 2',
        items: [{
            label: 'Station 1',
            locationLabel: 'placeholder',
            hint1: 'bla',
            hint2: 'blaaabluuub',
            solution: 'langweilig'
        }, {
            label: 'Station 2',
            locationLabel: 'placeholder',
            hint1: 'blablub',
            hint2: 'blaaabluuub',
            solution: 'langweilig'
        }]
    }]
</script>

<style>
</style>

<template>
    <div class="container mx-auto px-1 md:px-4">
        <h1 class="w-full mt-4 mb-4 text-6xl">
            Hints
        </h1>
        <UAccordion color="gray"
        variant="solid"
        size="xl"
        :items="items">
            <template #item="{ item }">
                <UAccordion color="gray"
                variant="ghost"
                size="md"
                :items="item.items">
                    <template #item="{ item }">
                        <RevealText label="Location" :value="item.locationLabel" />
                        <RevealText label="Hint1" :value="item.hint1" />
                        <RevealText label="Hint2" :value="item.hint2" />
                        <RevealText label="Solution" :value="item.solution" />
                    </template>
                </UAccordion>
            </template>
        </UAccordion>
    </div>
</template>

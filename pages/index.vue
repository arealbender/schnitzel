<script setup lang="ts">
    const items = [{
        label: 'Tag 1',
        items: [{
            label: 'Station 1',
            locationLabel: 'Wald Kirche',
            hint1: 'haste',
            hint2: 'ja schon',
            solution: 'gelöst <3'
        }, {
            label: 'Station 2',
            locationLabel: 'Jahnkampfbahn',
            hint1: ' versteckt hinter dem was du verlässt',
            hint2: 'ortsschild',
            solution: 'Hinter dem Schild auf dem Wald steht, geklebt an die rechte seite'
        }]
    }, {
        label: 'Tag 2',
        items: [{
            label: 'Station 1',
            locationLabel: 'Botanischer Garten',
            hint1: 'such was fehlt',
            hint2: 'im Insekt - versteckt',
            solution: 'Im Kopf des Grashüpfers'
        }, {
            label: 'Station 2',
            locationLabel: 'Bärenloch',
            hint1: ' was schon fast tot, erklimm zur Not',
            hint2: 'ein 3d gedrucktes Teil erbouldern',
            solution: 'im Toten Baum neben dem Volleyballplatz hochklettern und oben zwischen den Ästen das Teil suchen'
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

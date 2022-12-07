<template>
  <div class="container flex flex-col">
    <div class="w-full hid">
      ------------------------------------------------------------------------------------------------------------------
    </div>
    <div class="text-center">
      <component :is="Object.values(msgList)[j]"></component>
    </div>
    <div class="w-full hid">
      ------------------------------------------------------------------------------------------------------------------
    </div>
    <div class="text-center">
      <component :is="Object.values(animalList)[innerWidth]"></component>
    </div>
  </div>
</template>

<script setup>
import DocumentationIcon from './icons/IconDocumentation.vue'
import Cat from './icons/Cat.vue'
import Rabbit from './icons/Rabbit.vue'
import Rab2 from './icons/Rab2.vue'
import Tho from './icons/Tho.vue'
import ToolingIcon from './icons/IconTooling.vue'
import EcosystemIcon from './icons/IconEcosystem.vue'
import CommunityIcon from './icons/IconCommunity.vue'
import { ref, onBeforeMount } from 'vue'

const animalList = { Cat, Rab2, Rabbit, Tho };
const msgList = { DocumentationIcon, ToolingIcon, EcosystemIcon, CommunityIcon };

let i = ref(0);
onBeforeMount(() => {
  i = Math.floor(Math.random() * Object.values(animalList).length);
  return i
})

let j = ref(0);
onBeforeMount(() => {
  j = Math.floor(Math.random() * Object.values(msgList).length);
  return j
})

</script>

<style scoped>
.hid {
  white-space: nowrap;
  overflow: hidden;
  text-overflow: clip;
}

.fixed-content {
  position: fixed;
  overflow-y: scroll;
}
</style>
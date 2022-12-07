<template>
  <div class="flex flex-col bg-[url('https://images.unsplash.com/photo-1419242902214-272b3f66ee7a?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1813&q=80')]
    bg-cover
    h-auto
    bg-fixed">
    <header class="container sticky top-0 bg-slate-200/50 shadow-lg shadow-black">
      <div class="uppercase py-2 text-center text-lg font-mono">
        <HelloWorld :msg="strReturn()" />
      </div>
    </header>
    <RouterView />
  </div>
</template>
<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'

const msg = ['Chái tim cho người yêu',
  'Chương nhắm á',
  'A bê xê ít y zét',
  'Trời ơi cú tui trời ơi',
  'Nhớ ăn sáng mỗi ngày',
  'Éc éc éc',
  'Hai ba con mực, anh yêu em cực',
  'Vì mình quá thích cậu rồi',
  'Phải nàm thao phải nàm thao'
]
const strReturn = () => {
  const i = Math.floor(Math.random() * msg.length)
  return msg[i]
}
</script>


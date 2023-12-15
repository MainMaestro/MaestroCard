<script setup >
import ProjectItem from './components/ProjectItem.vue'
import ThePhotoCard from './components/ThePhotoCard.vue'
import { CheckIcon } from '@heroicons/vue/24/solid'
</script>

<template >
  <div
    class="min-h-screen justify-center flex flex-col bg-cover bg-[url(src/components/icons/1.jpg)]"
  >
    <header class=""></header>
    <main class="flex flex-col bg-gradient-to-r from-yellow-100 to-purple-300 mx-5 rounded-3xl">
      <div class="self-center my-4">
        <ThePhotoCard />
      </div>
      <h2 class="text-center text-2xl mt-2">На данный момент знаю более или менее:</h2>
      <div class="p-2 text-center flex justify-center">
        <ul class="flex flex-col gap-1 text-xl">
          <li class="inline-flex"><CheckIcon class="w-4 mr-2" /> HTML/CSS/JS</li>
          <li class="inline-flex"><CheckIcon class="w-4 mr-2" /> C#</li>
          <li class="inline-flex"><CheckIcon class="w-4 mr-2" /> SQL</li>
        </ul>
      </div>

      <h2 class="text-center text-2xl mt-2">Мои проекты:</h2>
      <div class="p-2">
        <ul>
          <li v-for="p in projects" :key="p" class="m-2">
            <ProjectItem :name="p.name" :link="p.link" :description="p.description" />
          </li>
        </ul>
      </div>

      <div class="ml-5 mb-1">
        <h2 class="text-2xl">Обратная связь</h2>
        <div class="flex justify-between">
          <div class="flex items-center">
            <a
              class="flex items-center pr-2 hover:bg-slate-200 rounded-3xl"
              href="https://vk.com/m9estro"
            >
              <img class="w-9 h-9 mr-2" src="src/components/icons/vk.png" alt="" />
              VK
            </a>
            <a
              class="flex m-2 items-center pr-2 hover:bg-slate-200 rounded-3xl"
              href="https://github.com/MainMaestro"
            >
              <img class="w-12 h-12 mr-1" src="src/components/icons/git.png" alt="" />
              github
            </a>
          </div>
        </div>
      </div>

      <hr class="border-t-3 border-black" />
    </main>
    <footer class="m-2"></footer>
  </div>
</template>
<script>
const projects = [
  {
    name: 'ElectronicMarket',
    description: 'Онлайн-магазин электроники',
    link: 'https://github.com/MainMaestro/ElectronicMarket'
  },
  {
    name: 'PizzaExpress',
    description: 'Сайт Пиццерии',
    link: 'https://github.com/MainMaestro/PizzaExpress'
  }
]
</script>
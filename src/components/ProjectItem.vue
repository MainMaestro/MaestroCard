<template>
  <a
    :href="link"
    class="transition ease-in-out delay-150 w-40 bg-yellow-100 hover:-translate-y-1 border-purple-300 border-2 hover:scale-110 hover:bg-purple-300 py-2 px-4 duration-300 rounded-xl inline-block text-center m-1"
    >{{ name }}</a
  >
  -
  {{ description }}
</template>
<script>
export default {
  props: ['name', 'description', 'link']
}
</script>

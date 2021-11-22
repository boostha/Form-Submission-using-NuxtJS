<template>
  <main class="bg-gray-100">
    <div class="container flex justify-center items-center h-screen ">
      <h1 class="text-8xl">{{ heroItem.hero }}</h1>
    </div>
  </main>
</template>

<script>
export default {
  props: ['heroItem']
}
</script>
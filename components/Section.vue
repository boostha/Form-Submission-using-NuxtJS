<template>
  <main class="flex flex-col items-center justify-center gap-10 my-10">
    <div id="app">
      <form @submit.prevent="addIdea()">
        <fieldset class="flex flex-col gap-2 items-start justify-center border-solid border-2 p-10">
          <legend class="text-2xl">Add Your Ideas Below</legend>
          <label for="idea-title" class="text-xl">Idea Title</label>
          <input type="text" name="idea-title" v-model="idea.title" class="border-solid border-2 p-1">
          <label for="idea-description" class="text-xl">Idea Description</label>
          <input type="text" name="idea-description" v-model="idea.description" class="border-solid border-2 p-1">
          <button class="bg-red-300 py-1 px-4 mt-4 rounded" type="submit">Add Idea</button>
        </fieldset>
      </form>
    </div>

    <section class=" flex flex-col gap-10">
      <h2 class="text-4xl border-b-2">Ideas</h2>

      <ul class="flex flex-col gap-10">
        <li v-for="item in ideas" :key="item.id" class="text-xl">
          <div class="border-solid border-2">
            <h3 class="bg-gray-200 px-4">{{ item.title }} </h3>
            <p class="px-4">{{ item.description }} </p>
          </div>
          <div class="flex gap-2">
            <button v-on:click="item.counter += 1">Like:</button>
            <p>{{item.counter}}</p>
          </div>
        </li>
      </ul>
    </section>
  </main>
</template>

<script>
export default {
  el: '#app',
  data() {
    return {
      idea: {
        title: "",
        description: "",
        counter: 0,
      },

      ideas: [],

      
    }
  },
  methods : {
    addIdea: function() {

      return this.ideas.push({
        title: this.idea.title,
        description: this.idea.description,
        counter: this.idea.counter
      })
    },

    onSubmit: function(event) {
      event.preventDefault()
    }
  },
}
</script>
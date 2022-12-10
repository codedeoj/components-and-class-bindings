<script setup>
  const cards = [
    {
      info: {
        title: "Card One",
        description: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptas quam reiciendis sit obcaecati natus fugiat. Cumque placeat eum debitis blanditiis."
      },
      colors: {
        bgLight: "bg-purple-500",
        bgDark: "bg-purple-600",
        textLight: "text-gray-600",
        textDark: "text-gray-800"
      },
   },
   {
      info: {
        title: "Card Two",
        description: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Omnis voluptates aperiam a unde eligendi cumque repellendus quidem quo, reprehenderit quis!"
      },
      colors: {
        bgLight: "bg-green-500",
        bgDark: "bg-green-600",
        textLight: "text-gray-600",
        textDark: "text-gray-800"
      },
  },
  {
      info: {
        title: "Card Three",
        description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quia vero dolorum consequuntur nisi dicta, corporis tempora maxime numquam veniam. Hic?"
    },
    colors: {
        bgLight: "bg-red-500",
        bgDark: "bg-red-600",
        textLight: "text-gray-600",
        textDark: "text-gray-800"
      },
  },
  ]
</script>

<template>
  <main>
    <h1 class="text-center font-bold text-2xl my-5">Home Page</h1>
    <div class="flex justify-center flex-wrap gap-5 mx-5">
      <AppCard 
      v-for="card in cards"
      :key="card.id"
      :info="card.info"
      :colors="card.colors"
      />
    </div>
  </main>
</template>


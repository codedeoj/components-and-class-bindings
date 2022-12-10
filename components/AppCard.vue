<script setup>
  defineProps({
    info: {
      type: Object,
      default() {
        return {
          title: "This is a Card Title",
          description: "Card Description Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequuntur, ipsam."
        };
      },
    },
    colors: {
    type: Object,
    default() {
      return {
        bgLight: "bg-blue-500",
        bgDark: "bg-blue-600",
        textLight: "text-gray-600",
        textDark: "text-gray-800",
      };
    },
  },
  })
</script>

<template>
    <article class="max-w-sm shadow-xl my-10 hover:scale-95 duration-300">
      <img src="https://cdn.pixabay.com/photo/2018/04/11/11/54/small-poly-3310319_960_720.jpg" alt="A picture of an eagle">
      <div class="py-6 px-8">
        <h3 
          :class="colors.textDark" 
          class="font-bold text-xl">
          {{ info.title }}
        </h3>
        <p 
          :class="colors.textLight"
          class="mt-4">
          {{ info.description }}
        </p>
      </div>
    </article>
</template>
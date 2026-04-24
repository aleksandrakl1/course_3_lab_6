<script setup>
import { ref } from "vue";
import UserAvatar from "./UserAvatar.vue";
import UserCard from "./UserCard.vue";

const name = ref("Артём Иванов");
</script>

<template>
  <div
    style="
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 16px;
      padding: 40px;
      font-family: sans-serif;
    "
  >
    <UserAvatar :name="name" />
    <UserCard :name="name" @name-changed="name = $event" />
  </div>
</template>

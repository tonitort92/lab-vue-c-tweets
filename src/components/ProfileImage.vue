<script setup>

    const props = defineProps({
    profileImage:String
})

</script>

<template>

    <img
      :src='profileImage'
      class="profile"
      alt="profile"
    />

</template>
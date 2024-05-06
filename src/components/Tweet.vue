<script setup>

import Actions from './Actions.vue';
import Timestamp from './Timestamp.vue';
import Handle from './Handle.vue';
import Message from './Message.vue'
import ProfileImage from './ProfileImage.vue'
import Name from './Name.vue'

const props = defineProps({
    message: String,
    profileImage: String,
    name:String,
    timestamp:String,
    handle:String
});

</script>

<template>
  <div class="tweet">
    <ProfileImage :profileImage='profileImage'/>

    <div class="body">
      <div class="top">
        <span class="user">
          <Name :name='name'/>
          <Handle :handle='handle'/>
        </span>

        <Timestamp :timestamp='timestamp'/>
      </div>

      <Message :message='message'/>

      <Actions/>
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<style scoped>
a {
  color: #42b983;
}
</style>

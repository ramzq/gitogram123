<template>
    <button class="c-story-user-item" @click="$emit('OnPress')">
        <div class="avatar">
            <img :src="avatar" class="img" alt="username avatar" />
        </div>
        <div class="username">{{ username }}</div>
    </button>
</template>
<script>
export default {
  props: {
    avatar: {
      type: String,
      requared: true
    },
    username: {
      type: String,
      requared: true
    }
  }
}
</script>
<style lang="scss" scoped src="./storyUserItem.scss"></style>

<template>
    <div class="topline">
        <topline>
            <template #headline>
            </template>
            <template #content>
                <ul class="stories">
                    <li class="stories-item" v-for="story in stories" :key="story.id">
                <story-user-item
                :avatar="story.avatar"
                :username="story.username"
                @onPress="handlePress(story.id)"
                />
                    </li>
                </ul>

            </template>
        </topline>
    </div>
</template>
<script>
import { topline } from '../../components/topline'
import StoryUserItem from '../../components/topline/storyUseritem'
import stories from './data.json'
export default {
  name: 'feeds',
  components: {
    topline, StoryUserItem
  },
  data () {
    return {
      stories
    }
  }
}
</script>
<style lang="scss" scoped src="./feeds.scss"></style>

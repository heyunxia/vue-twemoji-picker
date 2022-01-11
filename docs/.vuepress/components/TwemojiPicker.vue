<template>
   <div style="margin: 5% 0;">
    <twemoji-picker
      :emojiData="emojiDataAll"
      :emojiGroups="emojiGroups"
      :skinsSelection="false"
      :searchEmojisFeat="true"
      searchEmojiPlaceholder="Search here."
      searchEmojiNotFound="Searched emoji not found."
      isLoadingLabel="Loading..."
    ></twemoji-picker>
  </div>
</template>

<script>
import { TwemojiPicker }from '@heyunxia/vue-twemoji-picker';
import EmojiAllData from '@heyunxia/vue-twemoji-picker/emoji-data/en/emoji-all-groups.json';
import EmojiDataAnimalsNature from '@heyunxia/vue-twemoji-picker/emoji-data/en/emoji-group-animals-nature.json';
import EmojiDataFoodDrink from '@heyunxia/vue-twemoji-picker/emoji-data/en/emoji-group-food-drink.json';
import EmojiGroups from '@heyunxia/vue-twemoji-picker/emoji-data/emoji-groups.json';

export default {
  name: 'TwemojiPicker',
  components: {
    'twemoji-picker': TwemojiPicker
  },
  computed: {
    emojiDataAll() {
      return EmojiAllData;
    },
    emojiGroups() {
      return EmojiGroups;
    }
  }
}
</script>
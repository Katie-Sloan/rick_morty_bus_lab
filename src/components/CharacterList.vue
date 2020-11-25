<template lang="html">
  
      
      <div>
      <!-- <ul>
          <character-select v-for="(character, index) in characters" :character="character" :key="index"></character-select>
      </ul> -->
      <label for="character_select">Select a character:</label>
      <select id="character_select" v-model="selectedCharacter">
          <option disabled value="">Select a character</option>
          <option v-for="(character, index) in characters" :character="character" :key="index" :value="character">{{character.name}}</option>
      </select>
    </div>
    <div>
    <character-select></character-select>
    </div>
</template>

<script>
import CharacterSelect from './CharacterSelect.vue'


export default {
  name: 'character-list',
  props: ['characters', 'selectedCharacter'],
  components: { 
      "character-select": CharacterSelect 
  }
}
</script>

<style lang="css" scoped>

</style>
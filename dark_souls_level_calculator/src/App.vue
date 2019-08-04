<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <ClassSelection/>
    <LevelSection/>
    <AttributeSection/>
  </div>
</template>

<script>
import AttributeSection from './components/AttributesSection.vue'
import ClassSelection from './components/ClassSelection.vue'
import LevelSection from './components/LevelSection.vue'


export default {
  name: 'app',
  data: function() {
    return {
      classMap: {
        'bandit': {
          level: 4,
          vitality: 12,
          attunement: 8,
          endurance: 14,
          strength: 14,
          dexterity: 9,
          resistance: 11,
          intelligence: 8,	
          faith: 10
        },
        'cleric': {
          level: 2,
          vitality: 11,
          attunement: 11,
          endurance: 9,
          strength: 12,
          dexterity: 8,
          resistance: 11,
          intelligence: 8,	
          faith: 14
        },
        'deprived': {
          level: 6,
          vitality: 11,
          attunement: 11,
          endurance: 11,
          strength: 11,
          dexterity: 11,
          resistance: 11,
          intelligence: 11,	
          faith: 11
        },
        'hunter': {
          level: 4,
          vitality: 11,
          attunement: 9,
          endurance: 11,
          strength: 12,
          dexterity: 14,
          resistance: 11,
          intelligence: 9,	
          faith: 9
        },
        'knight': {
          level: 5,
          vitality: 14,
          attunement: 10,
          endurance: 10,
          strength: 11,
          dexterity: 11,
          resistance: 10,
          intelligence: 9,	
          faith: 11
        },
        'pyromancer': {
          level: 1,
          vitality: 10,
          attunement: 12,
          endurance: 11,
          strength: 12,
          dexterity: 9,
          resistance: 12,
          intelligence: 10,	
          faith: 8
        },
        'sorcerer': {
          level: 3,
          vitality: 8,
          attunement: 15,
          endurance: 8,
          strength: 9,
          dexterity: 11,
          resistance: 8,
          intelligence: 15,	
          faith: 8
        },
        'thief': {
          level: 5,
          vitality: 9,
          attunement: 9,
          endurance: 11,
          strength: 9,
          dexterity: 15,
          resistance: 10,
          intelligence: 12,	
          faith: 11
        },
        'wanderer': {
          level: 3,
          vitality: 10,
          attunement: 11,
          endurance: 10,
          strength: 10,
          dexterity: 14,
          resistance: 12,
          intelligence: 11,	
          faith: 8
        },
        'warrior': {
          level: 3,
          vitality: 11,
          attunement: 8,
          endurance: 12,
          strength: 13,
          dexterity: 13,
          resistance: 11,
          intelligence: 9,	
          faith: 9
        }
      },
      defaultClass: 'bandit',
      gainedStats: {
        level: 0,
        vitality: 0,
        attunement: 0,
        endurance: 0,
        strength: 0,
        dexterity: 0,
        resistance: 0,
        intelligence: 0,	
        faith: 0
      }
    }
  },
  components: {
    AttributeSection,
    ClassSelection,
    LevelSection,
  },
  computed: {
    startingStats: function() {
      let characterClass = this.getCurrentClass;
      return this.classMap[characterClass]
    },
    getCurrentClass: function() {
        if (this.currentClass == null) {
            return this.defaultClass
        } else {
          return this.currentClass
        }
    },
    getCurrentStats: function() {
      var currentStats = {}
      for (var key in this.startingStats) {
        currentStats[key] = this.startingStats[key] + this.gainedStats[key]
      }
      return currentStats
    }
  },
  methods: {
    levelUp: function(stat) {
      this.gainedStats.level++
      this.gainedStats[stat]++
    },
    levelDown: function(stat) {
      if(this.gainedStats.level === 0){
        if(this.gainedStats[stat] != 0){
          this.gainedStats[stat]--;   
        }
      }else {
      this.gainedStats.level--;
      this.gainedStats[stat]--;
      }
    },
    getStartingStat: function(stat) {
      let characterClass = this.getCurrentClass
      return this.classMap[characterClass][stat]
    },
    getCurrentStat: function(stat) {
      return this.startingStats[stat] + this.gainedStats[stat]
    },
    updateClass: function(newClass) {
      // There is a bug here. 
      // After a few clicks it stops working. Everytime it is random. Once 16 times, the other 4 times. 
      this.defaultClass = newClass
      this.startingStats()
    },
    resetFilter: function() {
      this.classMap.reset()
  },
}
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

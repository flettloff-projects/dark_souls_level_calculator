<template>
    <div class="levels">
        <!-- <form id="level-form" v-on:submit="submitForm"> -->
        <form id="level-form">
        <table class="table">
            <thead>
                <tr>
                <th></th>
                <th>Starting</th>
                <th>Current</th>
                </tr>
                <tr>
                </tr>
                <Stat statName="level"/>
                <Stat statName="vitality"/>
                <Stat statName="attunement"/>
                <Stat statName="endurance"/>
                <Stat statName="strength"/>
                <Stat statName="dexterity"/>
                <Stat statName="resistance"/>
                <Stat statName="intelligence"/>
                <Stat statName="faith"/>
                <tr></tr>
            </thead>
        </table>
         <!-- <button v-on="resetForm" class="button">Reset</button> -->
        <table  class="table">
        <thead>
            <tr></tr>
            <tr></tr>
        <tr>
            <th>HP</th>
            <th></th>
            <th></th>
            <th><input placeholder="0" maxlength="3" size="3" ref="hpInput"></th>
        </tr>
        <tr>
            <th>Stamina</th>
            <th></th>
            <th></th>
            <th><input placeholder="0" maxlength="3" size="3" ref="staminaInput"></th>
        </tr>
        <tr>
            <th>Equipment Burden</th>
            <th></th>
            <th></th>
            <th><input placeholder="0" maxlength="3" size="3" ref="equipmentBurdenInput"></th>
        </tr>
        </thead>
        </table>
        </form>
    </div>
</template>

<script>
import Stat from './Stat.vue'

export default {
    name: 'LevelSection',
    components: {
        Stat,
    },
    methods: {
        resetForm: function() {
            this.$data.text = " "
        },
        getStartingStat: function(stat) {
            return this.$parent.startingStats[stat]
        },
        getGainedStat: function(stat) {
            return this.$parent.getCurrentStat(stat)
        },
        levelUp: function(stat) {
            this.$parent.levelUp(stat)
        },
        levelDown: function(stat) {
            this.$parent.levelDown(stat)
        }
    }
}

</script>

<style scopped>
   .resizeArrows {
        width: 15px;
        height: 17px;
   }
   .levels {
        border-style: solid;
        border-width: 5px;
        overflow: auto;
        padding: 50px;
        margin: 1%;
        white-space: nowrap;
        text-align: left;
        position: relative;
        text-size-adjust: 5px;
   }
    .input {
       text-align: left;
       position: relative;
       padding: 50px;
       text-size-adjust: 5px;
   }
   .button {
        width: 5%;
        margin-left: 14%;
        margin-bottom: 10px;

   }
   .table {
        width: 30px;
        border-spacing: 4px 1rem;
   }
</style>

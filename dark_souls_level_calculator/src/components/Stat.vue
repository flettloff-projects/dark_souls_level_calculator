<template>
    <tr>
        <th> {{ displayStat }}</th>
        <th>
            <input v-bind:value=startingStat maxlength="3" size="3" ref="levelcurr" text-align="center" readonly> 
        </th>
        <th>
            <input v-bind:value=currentStat maxlength="3" size="3" ref="levelinit" readonly> 
        </th>
        <div v-if="isLevelProp">
            <th>
                <img @click="levelUp" class="resizeArrows" src="../assets/buttons/uparrow.png">
            </th>
            <th>
                <img @click="levelDown" class="resizeArrows" src="../assets/buttons/downarrow.png">
            </th> 
        </div>
    </tr>
</template>

<script>
export default {
    name: 'Stat',
    props: {
        statName: String
    },
    computed: {
        isLevelProp: function() {
            if (this.$props.statName === "level"){
                return false
            }  
            return true
        },
        displayStat: function() {
            return  this.$props.statName.charAt(0).toUpperCase() + this.$props.statName.slice(1)
        },
        startingStat: function() {
            return this.$parent.getStartingStat(this.$props.statName)
        },
        currentStat: function() {
            return this.$parent.getGainedStat(this.$props.statName)
        }
    },
    methods: {
        levelUp: function() {
            this.$parent.levelUp(this.$props.statName)
        },
        levelDown: function() {
            this.$parent.levelDown(this.$props.statName)
        }
    }
}
</script>

<style>
    .input {
       text-align: left;
       position: relative;
       padding: 50px;
       text-size-adjust: 5px;
   }
</style>
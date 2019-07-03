<template>
    <div class="levels">
        <form id="level-form" v-on:submit="submitForm">
        <table class="table">
            <thead>
                <tr>
                <th></th>
                <th>Starting</th>
                <th>Current</th>
                </tr>
                <tr>
                </tr>
                <tr>
                    <th>Level </th>
                    <th>
                       <input v-model="message" placeholder="0" maxlength="3" size="1" ref="levelinit"> 
                    </th>
                    <th>
                       <input v-model="message" placeholder="0" maxlength="3" size="1" ref="levelcurr"> 
                    </th>
                    <th>
                        <img class="resizeArrows" src="../assets/buttons/downarrow.png">
                    </th>
                    <th>
                        <img class="resizeArrows" src="../assets/buttons/uparrow.png">
                    </th> 
                </tr>
                <tr>
                    <th>Vitality </th>
                    <th>
                      <input v-model="message" :disabled="true" placeholder="0" maxlength="3" size="1"  type="Text" text-align="center" ref="vitalityinit">
                    </th>
                    <th>
                       <input v-model="message" placeholder="0" maxlength="3" size="1" ref="vitalityInput"> 
                    </th>
                    <th>
                        <img class="resizeArrows" src="../assets/buttons/downarrow.png">
                    </th>
                    <th>
                        <img class="resizeArrows" src="../assets/buttons/uparrow.png">
                    </th> 
                </tr>
                <tr>
                    <th>Attunement </th>
                    <th>
                      <input v-model="message" :disabled="true" placeholder="0" maxlength="3" size="1"  ref="attunementinit">
                    </th>
                    <th>
                       <input v-model="message" placeholder="0" maxlength="3" size="1" ref="attunementInput"> 
                    </th>
                    <th>
                        <img class="resizeArrows" src="../assets/buttons/downarrow.png">
                    </th>
                    <th>
                        <img class="resizeArrows" src="../assets/buttons/uparrow.png">
                    </th> 
                </tr>
                <tr>
                    <th>Endurance </th>
                    <th>
                      <input v-model="message"  :disabled="true" placeholder="0" maxlength="3" size="1" ref="enduranceinit">
                    </th>
                    <th>
                       <input v-model="message" placeholder="0" maxlength="3" size="1" ref="enduranceInput"> 
                    </th>
                    <th>
                        <img class="resizeArrows" src="../assets/buttons/downarrow.png">
                    </th>
                    <th>
                        <img class="resizeArrows" src="../assets/buttons/uparrow.png">
                    </th> 
                </tr>
                <tr>
                    <th>Strength </th>
                    <th>
                      <input v-model="message" :disabled="true" placeholder="0" maxlength="3" size="1"  ref="strengthinit"> 
                    </th>
                    <th>
                       <input v-model="message" placeholder="0" maxlength="3" size="1" ref="strengthInput"> 
                    </th>
                    <th>
                        <img class="resizeArrows" src="../assets/buttons/downarrow.png">
                    </th>
                    <th>
                        <img class="resizeArrows" src="../assets/buttons/uparrow.png">
                    </th> 
                </tr>
                <tr>
                    <th>Dexterity </th>
                    <th>
                      <input v-model="message" :disabled="true" placeholder="0" maxlength="3" size="1"  ref="dexterityinit"> 
                    </th>
                    <th>
                       <input v-model="message" placeholder="0" maxlength="3" size="1" ref="dexterityInput"> 
                    </th>
                    <th>
                        <img class="resizeArrows" src="../assets/buttons/downarrow.png">
                    </th>
                    <th>
                        <img class="resizeArrows" src="../assets/buttons/uparrow.png">
                    </th> 
                </tr>
                    <tr>
                    <th>Resistance </th>
                    <th>
                      <input v-model="message" :disabled="true" placeholder="0" maxlength="3" size="1" ref="resistanceinit"> 
                    </th>
                    <th>
                       <input v-model="message" placeholder="0" maxlength="3" size="1" ref="resistanceInput"> 
                    </th>
                    <th>
                        <img class="resizeArrows" src="../assets/buttons/downarrow.png">
                    </th>
                    <th>
                        <img class="resizeArrows" src="../assets/buttons/uparrow.png">
                    </th> 
                </tr>
                <tr>
                    <th>Intelligence </th>
                    <th>
                      <input v-model="message" :disabled="true" placeholder="0" maxlength="3" size="1" ref="intelligenceinit">
                    </th>
                    <th>
                       <input v-model="message" placeholder="0" maxlength="3" size="1" ref="intelligenceInput"> 
                    </th>
                    <th>
                        <img class="resizeArrows" src="../assets/buttons/downarrow.png">
                    </th>
                    <th>
                        <img class="resizeArrows" src="../assets/buttons/uparrow.png">
                    </th> 
                </tr>
                <tr>
                    <th>Faith </th>
                    <th>
                      <input v-model="message" :disabled="true" placeholder="0" maxlength="3" size="1"  ref="faithinit">
                    </th>
                    <th>
                       <input v-model="message" placeholder="0" maxlength="3" size="1" ref="faithInput"> 
                    </th>
                    <th>
                        <img class="resizeArrows" src="../assets/buttons/downarrow.png">
                    </th>
                    <th>
                        <img class="resizeArrows" src="../assets/buttons/uparrow.png">
                    </th> 
                </tr>
                <tr></tr>
            </thead>
        </table>
         <button v-on="resetForm" class="button">Reset</button>
        <table  class="table">
        <thead>
            <tr></tr>
            <tr></tr>
        <tr>
            <th>HP</th>
            <th></th>
            <th></th>
            <th><input v-model="message" placeholder="0" maxlength="3" size="1" ref="hpInput"></th>
        </tr>
        <tr>
            <th>Stamina</th>
            <th></th>
            <th></th>
            <th><input v-model="message" placeholder="0" maxlength="3" size="1" ref="staminaInput"></th>
        </tr>
        <tr>
            <th>Equipment Burden</th>
            <th></th>
            <th></th>
            <th><input v-model="message" placeholder="0" maxlength="3" size="1" ref="equipmentBurdenInput"></th>
        </tr>
        </thead>
        </table>
        </form>
    </div>
</template>

<script>
export default {
    name: 'LevelSection',
    methods: {
        resetForm: function() {
            this.$data.text = " "
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

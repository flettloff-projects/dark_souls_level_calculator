<template>
    <div class="levels">
        <form id="level-form" v-on:submit="submitForm">
        <table>
            <thead>
                <tr>
                    <th></th>
                    <th>
                     <label for="Level" type="Text">Level </label>
                     </th>
                     <th>
    <input v-model="message" placeholder="0" maxlength="3" size="1">
    </th>
    <th></th>
                </tr>
                <tr>
                    <th></th>
                <th>Starting</th>
                <th></th>
                <th>Current</th>
                <th></th>
                </tr>
                <th></th>
                <tr>
                    <th>Vitality </th>
                    <th>
                      <label for="Level" type="Text" text-align="center" ref="vitalityinit">0</label>  
                    </th>
                    <th></th>
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
                      <label for="Level" type="Text" text-align="center" ref="attunementinit">0</label>
                    </th>
                    <th></th>
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
                      <label for="Level" type="Text" text-align="center" ref="enduranceinit">0</label>  
                    </th>
                    <th></th>
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
                      <label for="Level" type="Text" text-align="center" ref="strengthinit">0</label>  
                    </th>
                    <th></th>
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
                      <label for="Level" type="Text" text-align="center" ref="dexterityinit">0</label>  
                    </th>
                    <th></th>
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
                      <label for="Level" type="Text" text-align="center" ref="resistanceinit">0</label>  
                    </th>
                    <th></th>
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
                      <label for="Level" type="Text" text-align="center" ref="intelligenceinit">0</label>  
                    </th>
                    <th></th>
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
                      <label for="Level" type="Text" text-align="center" ref="faithinit">0</label>  
                    </th>
                    <th></th>
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
                <tr>
                    <th></th>
                    <th></th>
                    <th></th>
                    <th></th>
                    <th>
                         <button v-on="resetForm">Reset</button>
                    </th>
                    <th></th>
                </tr>
            </thead>
        </table>
        <table>
        <thead>
        <tr>
            <th>HP</th>
            <th></th>
            <th><input v-model="message" placeholder="0" maxlength="3" size="1" ref="hpInput"></th>
        </tr>
        <tr>
            <th>Stamina</th>
            <th></th>
            <th><input v-model="message" placeholder="0" maxlength="3" size="1" ref="staminaInput"></th>
        </tr>
        <tr>
            <th>Equipment Burden</th>
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
        width: 10px;
        height: 12px;

   }
   .levels {
       border-style: solid;
        border-width: 5px;
        overflow: auto;
        padding: 30px;
        white-space: nowrap;
   }
   /* label = initial value */
   .label { 
       text-align: center;
       position: relative;
       padding: 50px;
       text-size-adjust: 5px;
   }
</style>

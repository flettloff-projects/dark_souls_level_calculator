<template>
    <div class="attributes">
        <form id="attributes-form" v-on:submit="submitForm">
            <table class="tableSoul">
                <thead>
                    <tr>
                        <th>Physical Defense</th>
                        <th><input placeholder="0" maxlength="3" size="1" ref="physicalDefenseBox"></th>
                        <th>Poise</th>
                        <th><input placeholder="0" maxlength="3" size="1" ref="poiseBox"></th>
                    </tr>
                    <tr>
                        <th>VS Strike</th>
                        <th><input placeholder="0" maxlength="3" size="1" ref="vsStrikehBox"></th>
                        <th>Bleed Resist</th>
                        <th><input placeholder="0" maxlength="3" size="1" ref="bleedResistBox"></th>
                    </tr>
                    <tr>
                        <th>VS Slash</th>
                        <th><input placeholder="0" maxlength="3" size="1" ref="vsSlashBox"></th>
                        <th>Poison Resist</th>
                        <th><input placeholder="0" maxlength="3" size="1" ref="poisonResistBox"></th>
                    </tr>
                    <tr>
                        <th>VS Blunt</th>
                        <th><input placeholder="0" maxlength="3" size="1" ref="vsBluntBox"></th>
                        <th>Curse Resist</th>
                        <th><input placeholder="0" maxlength="3" size="1" ref="curseResistBox"></th>
                    </tr>
                    <tr>
                        <th>Magic Def</th>
                        <th><input placeholder="0" maxlength="3" size="1" ref="magicDefenseBox"></th>
                        <th>Item Discovery</th>
                        <th><input placeholder="0" maxlength="3" size="1" ref="itemDiscoveryBox"></th>
                    </tr>
                    <tr>
                        <th>Flame Def</th>
                        <th><input placeholder="0" maxlength="3" size="1" ref="flameDefenseBox"></th>
                        <th>Attunement Slots</th>
                        <th><input placeholder="0" maxlength="3" size="1" ref="attunementSlotsBox"></th>
                    </tr>
                    <tr>
                        <th>Lightning Def</th>
                        <th><input placeholder="0" maxlength="3" size="1" ref="lighteningDefenseBox"></th>
                        <th></th>
                        <th></th>
                    </tr>
        </thead>
        </table>
        <table class="soul">
            <tr>
                <th>Souls to Next Level</th>
                <th></th>
                <th></th>
                <th>Total Souls Spent</th>
            </tr>
            <tr>
                <th><input class="soulInput" placeholder="0" maxlength="3" size="1" ref="soulsnextBox"></th>
                <th></th>
                <th></th>
                <th><input class="soulInput" placeholder="0" maxlength="3" size="1" ref="soulsspenttBox"></th>
            </tr>
        </table>
        </form>
    </div>
</template>


<style scopped>
   .attributes {
        padding: 50px;
        margin: 1%;
        white-space: nowrap;
        text-align: left;
        text-size-adjust: 5px;
        display: inline-block;
        position: absolute;
        left: 30%;
        top: 40%;
        z-index: -1;
        overflow: auto;
        white-space: nowrap;
   }
   .tableSoul {
        width: 30px;
        border-spacing: 50px 1rem;
   }
   .soul {
        width: 30px;
        border-spacing: 50px 2rem;
        margin: 2%; 
        padding: 50px;
        padding-left: 10px;
        padding-top: 85px;
   }
   .soulInput {
        margin-left: 35%;
        position: relative;
   }
</style>

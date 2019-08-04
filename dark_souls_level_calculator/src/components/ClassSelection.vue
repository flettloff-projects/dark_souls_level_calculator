<template>
    <div class="boxed">
        <img class="resize" hspace="10" vspace="10" v-on:click="updateClass('bandit')" src="../assets/class_images/bandit-starting-class-male-dark-souls.jpg">
        <img class="resize" hspace="10" vspace="10" v-on:click="updateClass('cleric')" src="../assets/class_images/cleric-starting-class-male-dark-souls.jpg">
        <img class="resize" hspace="10" vspace="10" v-on:click="updateClass('deprived')" src="../assets/class_images/deprived-starting-class-male-dark-souls.jpg">
        <img class="resize" hspace="10" vspace="10" v-on:click="updateClass('hunter')" src="../assets/class_images/hunter-starting-class-male-dark-souls.jpg">
        <img class="resize" hspace="10" vspace="10" v-on:click="updateClass('pyromancer')" src="../assets/class_images/pyromancer-starting-class-male-dark-souls.jpg">
        <img class="resize" hspace="10" vspace="10" v-on:click="updateClass('sorcerer')" src="../assets/class_images/sorcerer-starting-class-male-dark-souls.jpg">
        <img class="resize" hspace="10" vspace="10" v-on:click="updateClass('theif')" src="../assets/class_images/thief-starting-class-male-dark-souls.jpg">
        <img class="resize" hspace="10" vspace="10" v-on:click="updateClass('wanderer')" src="../assets/class_images/wanderer-starting-class-male-dark-souls.jpg">
        <img class="resize" hspace="10" vspace="10" v-on:click="updateClass('warrior')" src="../assets/class_images/warrior-starting-class-male-dark-souls.jpg">
        <img class="resize" hspace="10" vspace="10" v-on:click="updateClass('knight')" src="../assets/class_images/knight-starting-class-male-dark-souls.jpg">
    </div>
</template>

<script> 

export default {
    name: 'ClassSelection',
    methods: {
    updateClass: function (newClass) {
    this.$parent.updateClass(newClass)
    },
    }
}

</script>

<style scopped>
   .resize {
        width: 100px;
        height: 150px;

   }
   .boxed {
       border-style: solid;
        border-width: 5px;
        overflow: auto;
        white-space: nowrap;
   }
</style>

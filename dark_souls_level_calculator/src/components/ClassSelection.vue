<template>
    <div class="boxed">
        <img class="resize" hspace="10" vspace="10" src="../assets/class_images/bandit-starting-class-male-dark-souls.jpg">
        <img class="resize" hspace="10" vspace="10" src="../assets/class_images/cleric-starting-class-male-dark-souls.jpg">
        <img class="resize" hspace="10" vspace="10" src="../assets/class_images/deprived-starting-class-male-dark-souls.jpg">
        <img class="resize" hspace="10" vspace="10" src="../assets/class_images/hunter-starting-class-male-dark-souls.jpg">
        <img class="resize" hspace="10" vspace="10" src="../assets/class_images/pyromancer-starting-class-male-dark-souls.jpg">
        <img class="resize" hspace="10" vspace="10" src="../assets/class_images/sorcerer-starting-class-male-dark-souls.jpg">
        <img class="resize" hspace="10" vspace="10" src="../assets/class_images/thief-starting-class-male-dark-souls.jpg">
        <img class="resize" hspace="10" vspace="10" src="../assets/class_images/wanderer-starting-class-male-dark-souls.jpg">
        <img class="resize" hspace="10" vspace="10" src="../assets/class_images/warrior-starting-class-male-dark-souls.jpg">
        <img class="resize" hspace="10" vspace="10" src="../assets/class_images/knight-starting-class-male-dark-souls.jpg">
    </div>
</template>

<script>
export default {
    name: 'ClassSelection'
    // methods: {
    //     getClassImages : function () {
    //         var fs = require('fs');
    //         var files = fs.readdirSync('./assets/class_images/');
    //         return files;
    //     }
    // },
    // computed: {
    //     classImages () {
    //         var fs = require('fs');
    //         var files = fs.readdirSync('./assets/class_images/');
    //         return files;
    //     }
    // }
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

<template>
  <h2>My Course Goal</h2>
  <!-- Task 1: Output your main course goal with help of the composition API -->
  <!-- Don't hardcode it into the template, instead hardcode it into the JS code -->
  <h3 :class="goal.toggleGoal" >OUTPUT COURSE GOAL : {{  goal.courseGoal }}</h3>
  <!-- Task 2: Toggle (show/ hide) the goal with help of the button  -->
  <button  @click='onToggleGoal' >Toggle Goal</button>
  <!-- Task 3: Manage data in three ways -->
  <!-- => Separate refs -->
  <!-- => Ref Object -->
  <!-- => Reactive Object -->
  <!-- Task 4: Also solve the assignment with the Options API -->
</template>

<script>
import { reactive } from 'vue';
export default {
  setup(){
  const goal = reactive({
  		courseGoal = "learn vue",
  		toggleGoal = "show"
  });

 function onToggleGoal(){
    if(this.goal.toggleGoal === 'show'){
    this.goal.toggleGoal === 'hide';
    }
    else{
    this.goal.toggleGoal === 'show';
    }
 }
  return {courseGoal, onToggleGoal};

  },
}
</script>

<style>
html {
  font-family: sans-serif;
}
body {
  margin: 3rem;
  text-align: center;
}
.show {
  visibility: visible;
}

.hide {
  visibility: hidden;
}
</style>
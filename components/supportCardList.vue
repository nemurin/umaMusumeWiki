<template>
<div>
<div v-for="skill in skills"
       :key="skill.Title1" class="condition"
       v-if="isActive === true">
   <h4>{{skill.Title1}}</h4>
   <table>
  <tbody>
    <tr>
      <th class="select1">{{skill.Choices1}}</th>
      <td>{{skill.Content1}}</td>
    </tr>
    <tr>
      <th class="select2">{{skill.Choices2}}</th>
      <td>{{skill.Content2}}</td>
    </tr>
  </tbody>
</table>
</div> 
</div>
</template>

<script>
export default {
 props: ['skills','isActive']
}
</script>

<style>
@import './style.css';
</style>
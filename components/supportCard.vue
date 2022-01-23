<template>
<div>
	<div v-for="skill in skills"
       :key="skill.Title1" class="condition">
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
		data: function(){
    return {
     skills: [
       { Title1: '賢さブルボン 他人に危害を及ぼしてはならない',
      Choices1: 'すごく重そうだ',
      Content1: '体力-10、スタミナ+5、パワー+15',
      Choices2: '夜だと、音が少し響くかもな',
      Content2: '体力+10,賢さ+5' },
      { Title1: '賢さブルボン ステータス『つまらない？』',
      Choices1: '今のままでいいと思う',
      Content1: 'スピード+10,『勢い任せ』のヒントLv+1',
      Choices2: '表情を変えずに済む仮装は',
      Content2: '賢さ+15' },
      { Title1: '賢さブルボン 命令は守らなければならない',
      Choices1: '開店直前から待機しておこう',
      Content1: '『集中力』のヒントLv+1',
      Choices2: '昼休みになったらダッシュ',
      Content2: 'スピード+10スキルPt+15' },
     ],
  }
  },
	};
</script>
<style>
h4 {  
    padding: 0px 0 0px 40px;
    background-size: 25px 25px;
    color: inherit;
    background-repeat: no-repeat;
    background-position: left center;
    margin: 15px 0 10px;
    display: block;
    margin-block-start: 1.33em;
    margin-block-end: 0.33em;
    margin-inline-start: 0px;
    margin-inline-end: 0px;
    font-weight: bold;
}
tbody {
    display: table-row-group;
    vertical-align: middle;
    border-color: inherit;
}
table tr th {
    border: 1px solid #B1CEA6;
    background-color: #F5FCF2;
}
table tr td {
    border: 1px solid #B1CEA6;
    background-color: #FFF;
}
td {
    display: table-cell;
    vertical-align: inherit;
}
table {
    border-collapse: collapse;
    border-spacing: 0;
    margin-left: 40px;
}
.select1{
    background-color: #dcedc8!important;;
}
.select2{
    background-color: #fff9c4!important;
}
.condition{
    padding: 10px 0px 0px 00px;
}
</style>
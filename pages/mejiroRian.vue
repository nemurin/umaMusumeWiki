<template>
<div>
  <Header />
<div v-for="item in items"
       :key="item.Title1">
   <h4>{{item.Title1}}</h4>
   <table>
  <tbody>
    <tr>
      <th class="select1">{{item.Choices1}}</th>
      <td>{{item.Content1}}</td>
    </tr>
    <tr>
      <th class="select2">{{item.Choices2}}</th>
      <td>{{item.Content2}}</td>
    </tr>
  </tbody>
</table>
</div>       
</div>
</template>
<style>
body {
    margin: 0;
    padding: 0;
    color: #444;
    font-size: 14px;
    font-family: Hiragino Kaku Gothic Pro,"ヒラギノ角ゴ Pro W3",Meiryo,"メイリオ",Osaka,MS PGothic,arial,helvetica,sans-serif;
    line-height: 1.6;
    background: #FFF;
}
li {
    list-style: none;
}

h4 {  
    padding: 5px 0 5px 30px;
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
}
.select1{
    background-color: #dcedc8!important;;
}
.select2{
    background-color: #fff9c4!important;
}
</style>
<script>
export default {
  name: 'IndexPage',
  data: function(){
    return {
      items: [
       { Title1: '積み上げた本当のこと',
      Choices1: '君の力を見せてあげよう!',
      Content1: 'パワー＋10,スキルPt＋15',
      Choices2: '雨なんて吹き飛ばしてあげよう!',
      Content2: '「道悪○」のヒント＋1,スキルPt＋15' },
       { Title1: 'マッスルジェラシー',
      Choices1: '更に限界まで鍛えよう!',
      Content1: '根性+10',
      Choices2: 'まずは理論を教えてあげよう!',
      Content2: '賢さ+10' },
      { Title1: '本当の爽やかさ',
      Choices1: '演技じゃなく本物を見せるとか',
      Content1: 'スタミナ+20',
      Choices2: 'もっと躍動感を見せてみるとか',
      Content2: 'パワー+20' },
      { Title1: '周りから見た勝負服姿',
      Choices1: '魅力というのは積み重ねだ',
      Content1: '根性+20',
      Choices2: '君は充分に憧れの存在なんだ',
      Content2: 'スピード+20' },
     ]
  }
  }
}
</script>

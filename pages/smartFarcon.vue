<template>
<div>
  <Header />
<div v-for="item in items"
       :key="item.Title1" class="condition">
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
<SupportCard />
</div>
</template>

<script>
export default {
  name: 'IndexPage',
  data: function(){
    return {
      items: [
       { Title1: '畑でビルドアップ',
      Choices1: '雑草を抜いてしまおう',
      Content1: '根性+10',
      Choices2: '畑を耕そう',
      Content2: 'パワー+10' },
      { Title1: 'レースとグルメで満腹に',
      Choices1: '早めに行って観戦場所を確保しよう',
      Content1: '体力+10,スキルPt+15',
      Choices2: '人の隙間を見逃すな',
      Content2: '『軽やかステップ』のヒントLv+1' },
     ],
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
}
</script>
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
ul {
    margin-block-end: 15px;
}
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
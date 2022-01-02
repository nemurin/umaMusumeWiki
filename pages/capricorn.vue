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
<!-- 緑スキルチェック表 -->
<ul>左回り：
  <li v-for="(card, index) in filteredCards('左回り')" :key="index">
    <img v-bind:src="card.img">
    </li>
    </ul> 
<!-- 有効スキルチェック表 -->
      
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
    padding: 25px 0 5px 40px;
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
img {
    width: 50px;
    height: auto;
    vertical-align: inherit;
    list-style: none;
    top: 50%;
    content: '';
    border-left: 1px solid #f2f2f2;
    position: relative;
    display: block;
    float: left;
    text-align: center;
    cursor: pointer;
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
       { Title1: 'カプリコーン杯：高松宮記念',
      Choices1: '条件',
      Content1: '冬/中京/芝重/1200m(短距離)/左雪',
      Choices2: '考えたこと',
      Content2: 'エル→バクシン、オグリ→エアグル' },
     ],
     cards: [
       {
          id: 2,
          name: 'サイレンススズカSSR:スピード',
          greenSkill: '左回り',
          img: 'sp_2.png'
        },
        {
          id: 140,
          name: 'メジロアルダンSR:賢さ',
          greenSkill: '左回り',
          img: 'sp_140.png'
        },
        {
          id: 151,
          name: 'サイレンススズカSSR:スタミナ',
          greenSkill: '左回り',
          img: 'sp_151.png'
        },
        {
          id: 158,
          name: 'ゼンノロブロイSSR:スピード',
          greenSkill: '左回り',
          img: 'sp_158.png'
        },
        {
          id: 176,
          name: 'サイレンススズカSSR(ストーリー):スピード',
          greenSkill: '左回り',
          img: 'sp_176.png'
        },
        {
          id: 31,
          name: 'ユキノビジンSR:根性',
          greenSkill: '冬ウマ娘',
          img: 'sp_31.png'
        },
     ]
  }
  },
  computed: {
    filteredCards () {
      return function(filteredSkill) {
      let cards = []
      for(let i = 0; i < this.cards.length; i++) {
        let card = this.cards[i];
        if(card.greenSkill.indexOf(filteredSkill)!= -1){
          cards.push(card);
        }
      }
      return cards;
      }
    }
  },
}
</script>
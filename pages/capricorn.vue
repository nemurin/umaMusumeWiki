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
<!-- 有効スキルチェック表 -->
<div v-for="item in items"
       :key="item.Title1">
   <h4>バクシン：有効スキル</h4>
   <table>
  <tbody>
    <tr v-for="(skill, index) in ActiveSkills('左回り')" :key="index">
      <th class="select1">{{skill.name}}</th>
      <td>{{skill.greenSkill}}</td>
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
</div>
</template>

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
        {
          id: 31,
          name: 'ミホノブルボンSSR:賢さ',
          greenSkill: '雪の日',
          img: 'sp_31.png'
        },
     ],
     Ids: [
       {
          id: 2,
        },
        {
          id: 31,
        },
     ],
     Types: [
       {
          type: '左回り',
        },
        {
          type: '雪の日',
        },
     ],
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
    },
    ActiveSkills () {
      return function(Character) {
      let skills = []
      for(let k = 0; k < this.Ids.length; k++) {
      for(let j = 0; j < this.Types.length; j++) {
      for(let i = 0; i < this.cards.length; i++) {
        let skill = this.cards[i];
        let type = this.Types[j];
        let id = this.Ids[k];
        if(skill.greenSkill.indexOf(type.type)!= -1 && skill.id==id.id){
          skills.push(skill);
        }
      }
      }
      }
      return skills;
      }
    }
  },
}
</script>
<style>
@import './style.css';
</style>
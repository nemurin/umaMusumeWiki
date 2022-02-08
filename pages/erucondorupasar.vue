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
       { Title1: '勇気の入場曲',
      Choices1: 'ライブの曲を参考にしたら',
      Content1: 'パワー+20',
      Choices2: '応援団が使うような曲とか',
      Content2: 'スピード+10、パワー+10' },
      { Title1: '特大ピザを狙え',
      Choices1: '圧をかけていこう',
      Content1: 'パワー+10,スキルPt+15',
      Choices2: '人の隙間を見逃すな',
      Content2: '『軽やかステップ』のヒントLv+1' },
      { Title1: '世界最強の決意を',
      Choices1: 'ライバルたちに打ち勝つ',
      Content1: 'パワー+20',
      Choices2: '夢への決意とか',
      Content2: 'スタミナ+20' },
      { Title1: 'サボテン料理をご馳走デース',
      Choices1: 'ステーキかな',
      Content1: 'スピード+10,スタミナ+10',
      Choices2: 'スムージーがいいな',
      Content2: '賢さ+20' },
      { Title1: 'サルサ・ロハ',
      Choices1: 'いい汗をかけそうだ',
      Content1: 'スタミナ+10',
      Choices2: 'パワフルな響きだ',
      Content2: 'パワー+10' },
     ],
  }
  },
}
</script>
<style>
@import './style.css';
</style>
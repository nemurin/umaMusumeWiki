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
       { Title1: '研究対象はウマドル？',
      Choices1: 'ウマドルパワー、上がるといいな',
      Content1: 'パワー+10',
      Choices2: '研究って、どんなことをするんだ？',
      Content2: '賢さ+10' },
      { Title1: 'ドキドキ☆シチュエーション',
      Choices1: 'もっと全力でやってみよう',
      Content1: 'パワー+10',
      Choices2: '繰り返し練習あるのみ',
      Content2: 'スタミナ+10' },
      { Title1: '燃やせ☆ウマドル魂',
      Choices1: 'ファイト全開で頑張れ!',
      Content1: 'スタミナ+10根性+10',
      Choices2: '併走をお願いしてみよう',
      Content2: '『先頭プライド』のヒントLv+1' },
      { Title1: 'ダンスレッスン',
      Choices1: '地道に練習あるのみ',
      Content1: '根性+10',
      Choices2: 'スペシャルにアピールしよう',
      Content2: '賢さ+10' },
      { Title1: '磨いて☆DIAMOND',
      Choices1: 'キラキラになってみんなを魅了しよう!',
      Content1: 'スピード+20',
      Choices2: 'これからも切磋琢磨しよう!',
      Content2: 'パワー+10根性+10' },
      { Title1: 'ウマドル☆Friendship!',
      Choices1: '緊張を解いてあげられないかな',
      Content1: '賢さ+20',
      Choices2: '代わりに出てあげれば?',
      Content2: 'パワー+20' },
      { Title1: 'ドタバタ☆KIDSパニック!',
      Choices1: 'よし、アニメソングを歌おう!',
      Content1: 'スピード+20',
      Choices2: 'マジカル☆ダビ子ショーだ!',
      Content2: 'スタミナ+20' },
     ],
     plays: [
      { Title1: 'テストdeリカバリー☆',
      Choices1: '落ち着いて基礎を固めよう!',
      Content1: '賢さ+10',
      Choices2: 'ヤマカンで勝負だ!',
      Content2: 'パワー+10' },
      { Title1: 'シェアリング☆メモリー',
      Choices1: '2人で食べたからかも？',
      Content1: 'スタミナ+10',
      Choices2: 'お店も努力してるんだろうな',
      Content2: '根性+10' },
      { Title1: 'フューチャー☆ロケハン',
      Choices1: '……水族館!',
      Content1: '賢さ+10',
      Choices2: '……映画館!',
      Content2: 'パワー+10' },
      { Title1: '届いてforYou☆恩返し♪',
      Choices1: '俺も楽しいからいいんだよ',
      Content1: 'スピード+10',
      Choices2: 'ファル子が楽しんでくれれば満足だ',
      Content2: 'パワー+10' },
      { Title1: 'メモリー☆聖地巡礼',
      Choices1: 'ファールー子!ファールー子!',
      Content1: 'パワー+10',
      Choices2: '1歩ずつ成長できてるな/君の担当になれてよかった',
      Content2: '根性+10/スピード+10' },
     ],
  }
  },
}
</script>
<style>
@import './style.css';
</style>
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
</div>
</template>
<style>
@import './style.css';
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

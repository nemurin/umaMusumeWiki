<template>
<div>
  <div v-for="image in images" :key="image.name">
  <img v-bind:src=image.name v-on:click="onActive(image.function)" v-if="checkActive(image.function)">
  <img v-bind:src=image.name class="graymode" v-on:click="onActive(image.function)" v-if="checkActive(image.function) === false">
  </div>
  <div class="imaging">
  </div>

<SupportCardList :skills="skills159" :isActive="isActive"></SupportCardList>
<SupportCardList :skills="skills129" :isActive="isActive2"></SupportCardList>
<SupportCardList :skills="skills36" :isActive="isActive3"></SupportCardList>
<SupportCardList :skills="skills148" :isActive="isActive4"></SupportCardList>
<SupportCardList :skills="skills115" :isActive="isActive5"></SupportCardList>

</div>
</template>
<script>
	export default {
		data: function(){
    return {
     skills159: [
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
     skills129: [
       { Title1: '賢さドーベル やってみてもいい',
      Choices1: '体を鍛えて自信をつけよう!',
      Content1: '体力+15',
      Choices2: '鏡の前で笑顔の練習!',
      Content2: 'やる気アップ,スキルPt+15' },
      { Title1: '賢さドーベル 喜んでくれるかな……',
      Choices1: '別のプレゼントを探してみたら?',
      Content1: 'スキルPt+45',
      Choices2: '覚悟を決めて、突っ込もう!',
      Content2: '『負けん気』のヒントLv+1' },
      { Title1: '賢さドーベル 踏み出す、一歩',
      Choices1: 'チラシ、ください!!',
      Content1: '体力-10,スキルPt+15~45',
      Choices2: '一緒に配るぞ!',
      Content2: '根性+5,賢さ+5' },
     ],
     skills36: [
       { Title1: '賢さフクキタル お導きとお友だち',
      Choices1: 'みんなを信じて!',
      Content1: 'スキルPt+45',
      Choices2: '気分転換に、1度走る?',
      Content2: '体力-20(+10の場合有)『右回り◯』のヒントLv+1~3,ランダムでやる気アップ' },
      { Title1: '賢さフクキタル 信仰心と親切心が交わる時ーー',
      Choices1: '片っ端から作業を振ってみる',
      Content1: 'スキルPt+30',
      Choices2: '自分に親切にしてみるとかはどう?',
      Content2: '体力+20' },
      { Title1: '賢さフクキタル 全力スピリチュアル',
      Choices1: 'ただ急いでいるだけの気が……',
      Content1: '賢さ+5スキルPt+15',
      Choices2: 'もう少し気合いも込めてみたら?',
      Content2: '体力-10,スピード+5,スタミナ+5,パワー+5' },
     ],
     skills148: [
       { Title1: '賢さネイチャ 抑えられないキモチ',
      Choices1: '甘いお菓子を食べよう',
      Content1: '体力+10',
      Choices2: '走って頭をからっぽにしよう',
      Content2: '体力-5スピード+5パワー+5バッドコンディションが治る' },
      { Title1: '賢さネイチャ （ニャンとも）ガラじゃない',
      Choices1: '癒されることも大事だと伝える',
      Content1: '体力+20',
      Choices2: 'クレバーに入店する方法を伝える',
      Content2: '体力+10賢さ+5' },
      { Title1: '賢さネイチャ （美味しい）おせっかい',
      Choices1: '大根おろしで食べるペースアップ',
      Content1: '『ペースアップ』のヒントLv+1',
      Choices2: '寮で天ぷら祭りだ',
      Content2: 'やる気アップ、体力最大値+4' },
     ],
     skills115: [
       { Title1: 'パワーチケット 全・力・競・走',
      Choices1: '手すりショートカットだ',
      Content1: '『差しコーナー◯』のヒントLv+1',
      Choices2: '相手の動きを予想してみるとか',
      Content2: 'スキルPt+30' },
      { Title1: 'パワーチケット 全・力・筋・肉',
      Choices1: 'わかる!とことんやりたい',
      Content1: 'スタミナ+5スキルPt+15',
      Choices2: 'スポーツドリンクを渡す',
      Content2: 'やる気アップスキルPt+15' },
      
     ],
     isActive: true,
     isActive2: true,
     isActive3: true,
     isActive4: true,
     isActive5: true,
     images: [
          { name: 'sp_159.png',
            function: 'isActive'},
            { name: 'sp_129.png',
            function: 'isActive2'},
            { name: 'sp_36.png',
            function: 'isActive3'},
            { name: 'sp_148.png',
            function: 'isActive4'},
            { name: 'sp_115.png',
            function: 'isActive5'},
     ]
  }
  },
   methods: {
   onActive(name) {
        this[name] = !this[name]
      },
   checkActive(name) {
        if(this[name] === true){
          return true;
        }else{
          return false;
        }
      }

  },
	};
</script>
<style>
@import './style.css';
</style>
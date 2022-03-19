<template>
<div>
  <Header /> 

<div>
  <h1>sapoka</h1>
       <table>
  <tbody v-for="skill in skills"
       :key="skill.name" class="condition">
    <tr>
      <th class="select1">
        <img v-bind:src=skill.name>
        </th>
      <td>{{skill.GoodAtBonus}}</td>
      <td>{{skill.TrainingBonus}}</td>
      <td>{{skill.HintLV}}</td>
      <td>{{skill.HintBonus}}</td>
      <td>{{skill.InitialKizuna}}</td>
      <td>{{skill.InitialKasikosa}}</td>
      <td>{{skill.RaceBonus}}</td>
      <td>{{skill.FunBonus}}</td>
      <td>{{skill.LifeBonus}}</td>
      <td>{{skill.InitialSpeed}}</td>
      <td>{{skill.skillPT}}</td>
      <td>{{skill.other}}</td>
      <td>{{skill.speedUP}}</td>
      <td>{{skill.kasikosaUP}}</td>
      <td>{{skill.DistanceType}}</td>
      <td>{{skill.RaceType}}</td>
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
        {
        name: 'sp_159.png',
        GoodAtBonus: '得意率',
        FriendBonus: '友情Bonus',
        MotivationBonus: 'やる気Bonus',
        TrainingBonus: 'トレBonus',
        KasikosaBonus: '賢さBonus',
        HintLV: 'HintLV',
        HintBonus: 'HintBonus',
        InitialKizuna: '初期絆',
        InitialKasikosa: '初期賢さ',
        RaceBonus: 'レスボ',
        FunBonus: 'ファンボ',
        LifeBonus: '回復量',
        SpeedBonus: 'スピボ',
        InitialSpeed: '初期Speed',
        skillPT: 'スキルPT',
        other: 'その他',
        speedUP: 'スピ上昇値',
        kasikosaUP: '賢さ上昇値',
        DistanceType: '距離適性',
        RaceType: '脚質適正',
      },
      {
        name: 'sp_159.png',
        GoodAtBonus: 20,
        FriendBonus: 20,
        MotivationBonus: 40,
        TrainingBonus: 5,
        KasikosaBonus: 0,
        HintLV: 0,
        HintBonus: 0,
        InitialKizuna: 20,
        InitialKasikosa: 30,
        RaceBonus: 5,
        FunBonus: 10,
        LifeBonus: 5,
        SpeedBonus: 1,
        InitialSpeed: 20,
        skillPT: 0,
        other: '',
        speedUP: 8,
        kasikosaUP: 16,
        DistanceType: '',
        RaceType: '逃げ',
      },
      {
        name: 'sp_129.png',
        GoodAtBonus: 35,
        FriendBonus: 30,
        MotivationBonus: 30,
        TrainingBonus: 5,
        KasikosaBonus: 1,
        HintLV: 0,
        HintBonus: 0,
        InitialKizuna: 20,
        InitialKasikosa: 0,
        RaceBonus: 10,
        FunBonus: 10,
        LifeBonus: 5,
        SpeedBonus: 0,
        InitialSpeed: 0,
        skillPT: 0,
        other: '',
        speedUP: 7,
        kasikosaUP: 19,
        DistanceType: '中距離',
        RaceType: '差し',
      },
      {
        name: 'sp_191.png',
        GoodAtBonus: 20,
        FriendBonus: 25,
        MotivationBonus: 0,
        TrainingBonus: 0,
        KasikosaBonus: 1,
        HintLV: 1,
        HintBonus: 20,
        InitialKizuna: 20,
        InitialKasikosa: 30,
        RaceBonus: 5,
        FunBonus: 10,
        LifeBonus: 5,
        SpeedBonus: 0,
        InitialSpeed: 0,
        skillPT: 1,
        other: '4種でトレ効果10',
        speedUP: 7,
        kasikosaUP: 19,
        DistanceType: '中距離',
        RaceType: '差し',
      },
      {
        name: 'sp_21.png',
        GoodAtBonus: 35,
        FriendBonus: 20,
        MotivationBonus: 50,
        TrainingBonus: 0,
        KasikosaBonus: 1,
        HintLV: 2,
        HintBonus: 40,
        InitialKizuna: 25,
        InitialKasikosa: 20,
        RaceBonus: 5,
        FunBonus: 10,
        LifeBonus: 4,
        SpeedBonus: 0,
        InitialSpeed: 0,
        skillPT: 1,
        other: '',
        speedUP: 6,
        kasikosaUP: 18,
        DistanceType: 'マイル',
        RaceType: '先行',
      },
      {
        name: 'sp_22.png',
        GoodAtBonus: 50,
        FriendBonus: 30,
        MotivationBonus: 55,
        TrainingBonus: 0,
        KasikosaBonus: 1,
        HintLV: 2,
        HintBonus: 30,
        InitialKizuna: 40,
        InitialKasikosa: 0,
        RaceBonus: 5,
        FunBonus: 15,
        LifeBonus: 4,
        SpeedBonus: 0,
        InitialSpeed: 0,
        skillPT: 1,
        other: '',
        speedUP: 7,
        kasikosaUP: 19,
        DistanceType: 'マイル',
        RaceType: '先行',
      },
      {
        name: 'sp_32.png',
        GoodAtBonus: 50,
        FriendBonus: 20,
        MotivationBonus: 40,
        TrainingBonus: 5,
        KasikosaBonus: 1,
        HintLV: 0,
        HintBonus: 20,
        InitialKizuna: 25,
        InitialKasikosa: 20,
        RaceBonus: 10,
        FunBonus: 20,
        LifeBonus: 4,
        SpeedBonus: 0,
        InitialSpeed: 0,
        skillPT: 1,
        other: '',
        speedUP: 6,
        kasikosaUP: 18,
        DistanceType: '中距離',
        RaceType: '差し',
      },
      {
        name: 'sp_35.png',
        GoodAtBonus: 50,
        FriendBonus: 20,
        MotivationBonus: 55,
        TrainingBonus: 0,
        KasikosaBonus: 1,
        HintLV: 2,
        HintBonus: 30,
        InitialKizuna: 25,
        InitialKasikosa: 40,
        RaceBonus: 10,
        FunBonus: 20,
        LifeBonus: 4,
        SpeedBonus: 0,
        InitialSpeed: 0,
        skillPT: 0,
        other: '',
        speedUP: 6,
        kasikosaUP: 18,
        DistanceType: '汎用',
        RaceType: '汎用',
      },
      {
        name: 'sp_36.png',
        GoodAtBonus: 35,
        FriendBonus: 32,
        MotivationBonus: 50,
        TrainingBonus: 5,
        KasikosaBonus: 1,
        HintLV: 2,
        HintBonus: 40,
        InitialKizuna: 40,
        InitialKasikosa: 0,
        RaceBonus: 0,
        FunBonus: 0,
        LifeBonus: 4,
        SpeedBonus: 0,
        InitialSpeed: 0,
        skillPT: 0,
        other: '',
        speedUP: 7,
        kasikosaUP: 20,
        DistanceType: '汎用',
        RaceType: '差し',
      },
      {
        name: 'sp_38.png',
        GoodAtBonus: 0,
        FriendBonus: 20,
        MotivationBonus: 30,
        TrainingBonus: 15,
        KasikosaBonus: 1,
        HintLV: 2,
        HintBonus: 40,
        InitialKizuna: 30,
        InitialKasikosa: 40,
        RaceBonus: 5,
        FunBonus: 15,
        LifeBonus: 4,
        SpeedBonus: 0,
        InitialSpeed: 0,
        skillPT: 0,
        other: '',
        speedUP: 7,
        kasikosaUP: 20,
        DistanceType: '中距離',
        RaceType: '差し',
      },
      {
        name: 'sp_103.png',
        GoodAtBonus: 55,
        FriendBonus: 0,
        MotivationBonus: 10,
        TrainingBonus: 1,
        KasikosaBonus: 0,
        HintLV: 0,
        HintBonus: 0,
        InitialKizuna: 20,
        InitialKasikosa: 30,
        RaceBonus: 5,
        FunBonus: 15,
        LifeBonus: 0,
        SpeedBonus: 0,
        InitialSpeed: 0,
        skillPT: 1,
        other: '',
        speedUP: 6,
        kasikosaUP: 19,
        DistanceType: '中距離',
        RaceType: '差し',
      },
      {
        name: 'sp_107.png',
        GoodAtBonus: 0,
        FriendBonus: 20,
        MotivationBonus: 30,
        TrainingBonus: 15,
        KasikosaBonus: 1,
        HintLV: 0,
        HintBonus: 0,
        InitialKizuna: 30,
        InitialKasikosa: 20,
        RaceBonus: 5,
        FunBonus: 15,
        LifeBonus: 3,
        SpeedBonus: 0,
        InitialSpeed: 0,
        skillPT: 0,
        other: '',
        speedUP: 7,
        kasikosaUP: 20,
        DistanceType: '中距離',
        RaceType: '差し',
      },
     ],
  }
  },
   methods: {


  },
	};
</script>
<style>
@import './style.css';
img {
    width: 40px;
      height: auto;
      vertical-align: inherit;
      border-left: 1px solid #f2f2f2;
      float: left;
      text-align: center;
      cursor: pointer;  
  }
</style>
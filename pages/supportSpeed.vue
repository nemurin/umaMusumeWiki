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
      <td>{{skill.InitialSpeed}}</td>
      <td>{{skill.RaceBonus}}</td>
      <td>{{skill.FunBonus}}</td>
      <td>{{skill.InitialPower}}</td>
      <td>{{skill.skillPT}}</td>
      <td>{{skill.other}}</td>
      <td>{{skill.speedUP}}</td>
      <td>{{skill.powerUP}}</td>
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
        name: 'sp_108.png',
        GoodAtBonus: '得意率',
        FriendBonus: '友情Bonus',
        MotivationBonus: 'やる気Bonus',
        TrainingBonus: 'トレBonus',
        SpeedBonus: 'スピBonus',
        HintLV: 'HintLV',
        HintBonus: 'HintBonus',
        InitialKizuna: '初期絆',
        InitialSpeed: '初期スピ',
        RaceBonus: 'レスボ',
        FunBonus: 'ファンボ',
        LifeBonus: '回復量',
        SpeedBonus: 'スピボ',
        InitialPower: '初期パワ',
        skillPT: 'スキルPT',
        other: 'その他',
        speedUP: 'スピ上昇値',
        powerUP: 'パワ上昇値',
        DistanceType: '距離適性',
        RaceType: '脚質適正',
      },
      {
        name: 'sp_108.png',
        GoodAtBonus: 100,
        FriendBonus: 25,
        MotivationBonus: 30,
        TrainingBonus: 15,
        SpeedBonus: 0,
        HintLV: 2,
        HintBonus: 30,
        InitialKizuna: 35,
        InitialSpeed: 0,
        RaceBonus: 5,
        FunBonus: 15,
        PowerBonus: 1,
        InitialPower: 0,
        skillPT: 0,
        other: '',
        speedUP: 22,
        powerUP: 13,
        DistanceType: '長距離',
        RaceType: '逃げ',
      },
      {
        name: 'sp_137.png',
        GoodAtBonus: 0,
        FriendBonus: 25,
        MotivationBonus: 18,
        TrainingBonus: 8,
        SpeedBonus: 0,
        HintLV: 2,
        HintBonus: 50,
        InitialKizuna: 17,
        InitialSpeed: 0,
        RaceBonus: 0,
        FunBonus: 0,
        PowerBonus: 1,
        InitialPower: 0,
        skillPT: 1,
        other: '',
        speedUP: 21,
        powerUP: 12,
        DistanceType: '長距離',
        RaceType: '追込',
      },
      {
        name: 'sp_184.png',
        GoodAtBonus: 50,
        FriendBonus: 20,
        MotivationBonus: 0,
        TrainingBonus: 10,
        SpeedBonus: 1,
        HintLV: 0,
        HintBonus: 20,
        InitialKizuna: 25,
        InitialSpeed: 35,
        RaceBonus: 5,
        FunBonus: 10,
        PowerBonus: 0,
        InitialPower: 30,
        skillPT: 0,
        other: '',
        speedUP: 21,
        powerUP: 9,
        DistanceType: '中距離',
        RaceType: '先行',
      },
      {
        name: 'sp_18.png',
        GoodAtBonus: 0,
        FriendBonus: 18,
        MotivationBonus: 41,
        TrainingBonus: 8,
        SpeedBonus: 1,
        HintLV: 2,
        HintBonus: 45,
        InitialKizuna: 45,
        InitialSpeed: 0,
        RaceBonus: 5,
        FunBonus: 13,
        PowerBonus: 0,
        InitialPower: 30,
        skillPT: 0,
        other: '',
        speedUP: 22,
        powerUP: 10,
        DistanceType: '',
        RaceType: '先行',
      },
      {
        name: 'sp_33.png',
        GoodAtBonus: 35,
        FriendBonus: 20,
        MotivationBonus: 65,
        TrainingBonus: 5,
        SpeedBonus: 1,
        HintLV: 2,
        HintBonus: 40,
        InitialKizuna: 25,
        InitialSpeed: 0,
        RaceBonus: 5,
        FunBonus: 0,
        PowerBonus: 0,
        InitialPower: 0,
        skillPT: 0,
        other: '',
        speedUP: 22,
        powerUP: 10,
        DistanceType: '',
        RaceType: '差し',
      },
      {
        name: 'sp_34.png',
        GoodAtBonus: 20,
        FriendBonus: 20,
        MotivationBonus: 45,
        TrainingBonus: 10,
        SpeedBonus: 1,
        HintLV: 2,
        HintBonus: 40,
        InitialKizuna: 30,
        InitialSpeed: 20,
        RaceBonus: 5,
        FunBonus: 15,
        PowerBonus: 0,
        InitialPower: 0,
        skillPT: 0,
        other: '',
        speedUP: 23,
        powerUP: 10,
        DistanceType: '',
        RaceType: '追込',
      },
      {
        name: 'sp_95.png',
        GoodAtBonus: 50,
        FriendBonus: 30,
        MotivationBonus: 40,
        TrainingBonus: 10,
        SpeedBonus: 0,
        HintLV: 0,
        HintBonus: 20,
        InitialKizuna: 25,
        InitialSpeed: 0,
        RaceBonus: 5,
        FunBonus: 15,
        PowerBonus: 0,
        InitialPower: 0,
        skillPT: 1,
        other: '',
        speedUP: 23,
        powerUP: 11,
        DistanceType: '',
        RaceType: '追込',
      },
      {
        name: 'sp_40.png',
        GoodAtBonus: 60,
        FriendBonus: 20,
        MotivationBonus: 30,
        TrainingBonus: 5,
        SpeedBonus: 1,
        HintLV: 3,
        HintBonus: 50,
        InitialKizuna: 25,
        InitialSpeed: 20,
        RaceBonus: 0,
        FunBonus: 0,
        PowerBonus: 1,
        InitialPower: 0,
        skillPT: 0,
        other: '',
        speedUP: 21,
        powerUP: 11,
        DistanceType: '短距離',
        RaceType: '',
      },
      {
        name: 'sp_98.png',
        GoodAtBonus: 25,
        FriendBonus: 16,
        MotivationBonus: 60,
        TrainingBonus: 0,
        SpeedBonus: 1,
        HintLV: 2,
        HintBonus: 33,
        InitialKizuna: 21,
        InitialSpeed: 0,
        RaceBonus: 0,
        FunBonus: 0,
        PowerBonus: 0,
        InitialPower: 0,
        skillPT: 0,
        other: '',
        speedUP: 20,
        powerUP: 9,
        DistanceType: '',
        RaceType: '逃げ',
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
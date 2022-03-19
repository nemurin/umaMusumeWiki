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
      <td>{{skill.InitialPower}}</td>
      <td>{{skill.RaceBonus}}</td>
      <td>{{skill.FunBonus}}</td>
      <td>{{skill.InitialStamina}}</td>
      <td>{{skill.skillPT}}</td>
      <td>{{skill.other}}</td>
      <td>{{skill.powerUP}}</td>
      <td>{{skill.staminaUP}}</td>
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
        name: 'sp_115.png',
        GoodAtBonus: '得意率',
        FriendBonus: '友情Bonus',
        MotivationBonus: 'やる気Bonus',
        TrainingBonus: 'トレBonus',
        PowerBonus: 'パワBonus',
        HintLV: 'HintLV',
        HintBonus: 'HintBonus',
        InitialKizuna: '初期絆',
        InitialPower: '初期パワ',
        RaceBonus: 'レスボ',
        FunBonus: 'ファンボ',
        LifeBonus: '回復量',
        StaminaBonus: 'スタボ',
        InitialStamina: '初期スタ',
        skillPT: 'スキルPT',
        other: 'その他',
        powerUP: 'パワ上昇値',
        staminaUP: 'スタ上昇値',
        DistanceType: '距離適性',
        RaceType: '脚質適正',
      },
      {
        name: 'sp_115.png',
        GoodAtBonus: 35,
        FriendBonus: 32,
        MotivationBonus: 30,
        TrainingBonus: 5,
        PowerBonus: 1,
        HintLV: 2,
        HintBonus: 40,
        InitialKizuna: 45,
        InitialPower: 0,
        RaceBonus: 0,
        FunBonus: 0,
        StaminaBonus: 0,
        InitialStamina: 0,
        skillPT: 0,
        other: '',
        powerUP: 20,
        staminaUP: 11,
        DistanceType: '',
        RaceType: '差し',
      },
      {
        name: 'sp_7.png',
        GoodAtBonus: 70,
        FriendBonus: 32,
        MotivationBonus: 40,
        TrainingBonus: 5,
        PowerBonus: 1,
        HintLV: 0,
        HintBonus: 0,
        InitialKizuna: 25,
        InitialPower: 20,
        RaceBonus: 8,
        FunBonus: 18,
        StaminaBonus: 0,
        InitialStamina: 0,
        skillPT: 0,
        other: '',
        powerUP: 20,
        staminaUP: 11,
        DistanceType: '中距離',
        RaceType: '先行',
      },
      {
        name: 'sp_146.png',
        GoodAtBonus: 18,
        FriendBonus: 25,
        MotivationBonus: 0,
        TrainingBonus: 10,
        PowerBonus: 1,
        HintLV: 2,
        HintBonus: 30,
        InitialKizuna: 15,
        InitialPower: 48,
        RaceBonus: 0,
        FunBonus: 0,
        StaminaBonus: 0,
        InitialStamina: 0,
        skillPT: 0,
        other: '',
        powerUP: 19,
        staminaUP: 10,
        DistanceType: '中距離',
        RaceType: '先行',
      },
      {
        name: 'sp_172.png',
        GoodAtBonus: 0,
        FriendBonus: 37,
        MotivationBonus: 0,
        TrainingBonus: 0,
        PowerBonus: 0,
        HintLV: 0,
        HintBonus: 0,
        InitialKizuna: 20,
        InitialPower: 35,
        RaceBonus: 15,
        FunBonus: 20,
        StaminaBonus: 35,
        InitialStamina: 1,
        skillPT: 0,
        other: '',
        powerUP: 17,
        staminaUP: 12,
        DistanceType: '',
        RaceType: '逃げ',
      },
      {
        name: 'sp_152.png',
        GoodAtBonus: 35,
        FriendBonus: 25,
        MotivationBonus: 0,
        TrainingBonus: 5,
        PowerBonus: 0,
        HintLV: 1,
        HintBonus: 20,
        InitialKizuna: 15,
        InitialPower: 0,
        RaceBonus: 1,
        FunBonus: 5,
        StaminaBonus: 0,
        InitialStamina: 1,
        skillPT: 0,
        other: '',
        powerUP: 16,
        staminaUP: 11,
        DistanceType: '',
        RaceType: '',
      },
      {
        name: 'sp_116.png',
        GoodAtBonus: 20,
        FriendBonus: 16,
        MotivationBonus: 33,
        TrainingBonus: 10,
        PowerBonus: 1,
        HintLV: 2,
        HintBonus: 45,
        InitialKizuna: 16,
        InitialPower: 0,
        RaceBonus: 0,
        FunBonus: 0,
        StaminaBonus: 0,
        InitialStamina: 0,
        skillPT: 0,
        other: '',
        powerUP: 18,
        staminaUP: 10,
        DistanceType: '',
        RaceType: '',
      },
      {
        name: 'sp_23.png',
        GoodAtBonus: 50,
        FriendBonus: 43,
        MotivationBonus: 40,
        TrainingBonus: 0,
        PowerBonus: 0,
        HintLV: 0,
        HintBonus: 0,
        InitialKizuna: 25,
        InitialPower: 20,
        RaceBonus: 10,
        FunBonus: 15,
        StaminaBonus: 1,
        InitialStamina: 0,
        skillPT: 0,
        other: '',
        powerUP: 19,
        staminaUP: 13,
        DistanceType: '',
        RaceType: '追込',
      },
      {
        name: 'sp_25.png',
        GoodAtBonus: 0,
        FriendBonus: 32,
        MotivationBonus: 30,
        TrainingBonus: 10,
        PowerBonus: 0,
        HintLV: 2,
        HintBonus: 40,
        InitialKizuna: 30,
        InitialPower: 40,
        RaceBonus: 5,
        FunBonus: 15,
        StaminaBonus: 1,
        InitialStamina: 0,
        skillPT: 0,
        other: '',
        powerUP: 19,
        staminaUP: 11,
        DistanceType: 'マイル',
        RaceType: '',
      },
      {
        name: 'sp_29.png',
        GoodAtBonus: 50,
        FriendBonus: 43,
        MotivationBonus: 40,
        TrainingBonus: 0,
        PowerBonus: 1,
        HintLV: 0,
        HintBonus: 20,
        InitialKizuna: 25,
        InitialPower: 20,
        RaceBonus: 5,
        FunBonus: 15,
        StaminaBonus: 0,
        InitialStamina: 0,
        skillPT: 0,
        other: '',
        powerUP: 21,
        staminaUP: 11,
        DistanceType: '',
        RaceType: '逃げ',
      },
      {
        name: 'sp_29.png',
        GoodAtBonus: 0,
        FriendBonus: 20,
        MotivationBonus: 45,
        TrainingBonus: 5,
        PowerBonus: 0,
        HintLV: 3,
        HintBonus: 50,
        InitialKizuna: 25,
        InitialPower: 0,
        RaceBonus: 10,
        FunBonus: 10,
        StaminaBonus: 1,
        InitialStamina: 0,
        skillPT: 0,
        other: '',
        powerUP: 17,
        staminaUP: 11,
        DistanceType: '',
        RaceType: 'マイル',
      },
      {
        name: 'sp_26.png',
        GoodAtBonus: 60,
        FriendBonus: 20,
        MotivationBonus: 30,
        TrainingBonus: 15,
        PowerBonus: 0,
        HintLV: 2,
        HintBonus: 60,
        InitialKizuna: 30,
        InitialPower: 0,
        RaceBonus: 5,
        FunBonus: 15,
        StaminaBonus: 1,
        InitialStamina: 0,
        skillPT: 0,
        other: '',
        powerUP: 18,
        staminaUP: 12,
        DistanceType: '',
        RaceType: '',
      },
      {
        name: 'sp_190.png',
        GoodAtBonus: 0,
        FriendBonus: 25,
        MotivationBonus: 30,
        TrainingBonus: 5,
        PowerBonus: 0,
        HintLV: 2,
        HintBonus: 40,
        InitialKizuna: 0,
        InitialPower: 20,
        RaceBonus: 5,
        FunBonus: 10,
        StaminaBonus: 1,
        InitialStamina: 20,
        skillPT: 0,
        other: '',
        powerUP: 18,
        staminaUP: 12,
        DistanceType: '',
        RaceType: '',
      },
      {
        name: 'sp_99.png',
        GoodAtBonus: 70,
        FriendBonus: 20,
        MotivationBonus: 55,
        TrainingBonus: 0,
        PowerBonus: 1,
        HintLV: 2,
        HintBonus: 30,
        InitialKizuna: 25,
        InitialPower: 20,
        RaceBonus: 10,
        FunBonus: 20,
        StaminaBonus: 0,
        InitialStamina: 0,
        skillPT: 0,
        other: '',
        powerUP: 18,
        staminaUP: 9,
        DistanceType: '',
        RaceType: 'マイル',
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
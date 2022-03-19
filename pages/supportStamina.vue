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
      <td>{{skill.InitialStamina}}</td>
      <td>{{skill.RaceBonus}}</td>
      <td>{{skill.FunBonus}}</td>
      <td>{{skill.InitialKonjou}}</td>
      <td>{{skill.skillPT}}</td>
      <td>{{skill.other}}</td>
      <td>{{skill.staminaUP}}</td>
      <td>{{skill.konjouUP}}</td>
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
        name: 'sp_16.png',
        GoodAtBonus: '得意率',
        FriendBonus: '友情Bonus',
        MotivationBonus: 'やる気Bonus',
        TrainingBonus: 'トレBonus',
        StaminaBonus: 'スタBonus',
        HintLV: 'HintLV',
        HintBonus: 'HintBonus',
        InitialKizuna: '初期絆',
        InitialStamina: '初期スタ',
        RaceBonus: 'レスボ',
        FunBonus: 'ファンボ',
        LifeBonus: '回復量',
        KonjouBonus: '根性ボ',
        InitialKonjou: '初期根性',
        skillPT: 'スキルPT',
        other: 'その他',
        staminaUP: 'スタ上昇値',
        konjouUP: '根性上昇値',
        DistanceType: '距離適性',
        RaceType: '脚質適正',
      },
      {
        name: 'sp_16.png',
        GoodAtBonus: 55,
        FriendBonus: 33,
        MotivationBonus: 0,
        TrainingBonus: 11,
        StaminaBonus: 1,
        HintLV: 0,
        HintBonus: 0,
        InitialKizuna: 0,
        InitialStamina: 0,
        RaceBonus: 6,
        FunBonus: 16,
        KonjouBonus: 0,
        InitialKonjou: 0,
        skillPT: 0,
        other: '',
        staminaUP: 22,
        konjouUP: 9,
        DistanceType: '',
        RaceType: '',
      },
      {
        name: 'sp_16.png',
        GoodAtBonus: 55,
        FriendBonus: 37,
        MotivationBonus: 0,
        TrainingBonus: 15,
        StaminaBonus: 1,
        HintLV: 0,
        HintBonus: 0,
        InitialKizuna: 30,
        InitialStamina: 35,
        RaceBonus: 10,
        FunBonus: 20,
        KonjouBonus: 0,
        InitialKonjou: 0,
        skillPT: 0,
        other: '',
        staminaUP: 23,
        konjouUP: 9,
        DistanceType: '',
        RaceType: '',
      },
      {
        name: 'sp_151.png',
        GoodAtBonus: 35,
        FriendBonus: 25,
        MotivationBonus: 30,
        TrainingBonus: 5,
        StaminaBonus: 1,
        HintLV: 0,
        HintBonus: 0,
        InitialKizuna: 30,
        InitialStamina: 55,
        RaceBonus: 5,
        FunBonus: 10,
        KonjouBonus: 0,
        InitialKonjou: 0,
        skillPT: 0,
        other: '',
        staminaUP: 20,
        konjouUP: 8,
        DistanceType: '',
        RaceType: '逃げ',
      },
      {
        name: 'sp_92.png',
        GoodAtBonus: 50,
        FriendBonus: 30,
        MotivationBonus: 30,
        TrainingBonus: 0,
        StaminaBonus: 1,
        HintLV: 2,
        HintBonus: 10,
        InitialKizuna: 20,
        InitialStamina: 20,
        RaceBonus: 5,
        FunBonus: 10,
        KonjouBonus: 1,
        InitialKonjou: 0,
        skillPT: 0,
        other: '',
        staminaUP: 20,
        konjouUP: 10,
        DistanceType: '長距離',
        RaceType: '先行',
      },
      {
        name: 'sp_4.png',
        GoodAtBonus: 0,
        FriendBonus: 16,
        MotivationBonus: 23,
        TrainingBonus: 10,
        StaminaBonus: 1,
        HintLV: 2,
        HintBonus: 45,
        InitialKizuna: 36,
        InitialStamina: 0,
        RaceBonus: 0,
        FunBonus: 0,
        KonjouBonus: 0,
        InitialKonjou: 0,
        skillPT: 0,
        other: '',
        staminaUP: 20,
        konjouUP: 9,
        DistanceType: '長距離',
        RaceType: '追込',
      },
      {
        name: 'sp_189.png',
        GoodAtBonus: 50,
        FriendBonus: 25,
        MotivationBonus: 0,
        TrainingBonus: 0,
        StaminaBonus: 2,
        HintLV: 0,
        HintBonus: 0,
        InitialKizuna: 30,
        InitialStamina: 30,
        RaceBonus: 5,
        FunBonus: 10,
        KonjouBonus: 1,
        InitialKonjou: 0,
        skillPT: 0,
        other: '',
        staminaUP: 20,
        konjouUP: 9,
        DistanceType: '長距離',
        RaceType: '',
      },
      {
        name: 'sp_28.png',
        GoodAtBonus: 70,
        FriendBonus: 20,
        MotivationBonus: 40,
        TrainingBonus: 5,
        StaminaBonus: 1,
        HintLV: 2,
        HintBonus: 30,
        InitialKizuna: 25,
        InitialStamina: 20,
        RaceBonus: 10,
        FunBonus: 20,
        KonjouBonus: 0,
        InitialKonjou: 0,
        skillPT: 0,
        other: '',
        staminaUP: 20,
        konjouUP: 8,
        DistanceType: '長距離',
        RaceType: '',
      },
      {
        name: 'sp_27.png',
        GoodAtBonus: 55,
        FriendBonus: 37,
        MotivationBonus: 20,
        TrainingBonus: 10,
        StaminaBonus: 0,
        HintLV: 0,
        HintBonus: 0,
        InitialKizuna: 0,
        InitialStamina: 30,
        RaceBonus: 5,
        FunBonus: 15,
        KonjouBonus: 0,
        InitialKonjou: 0,
        skillPT: 1,
        other: '',
        staminaUP: 21,
        konjouUP: 9,
        DistanceType: '',
        RaceType: '',
      },
      {
        name: 'sp_117.png',
        GoodAtBonus: 60,
        FriendBonus: 32,
        MotivationBonus: 37,
        TrainingBonus: 5,
        StaminaBonus: 0,
        HintLV: 2,
        HintBonus: 47,
        InitialKizuna: 20,
        InitialStamina: 20,
        RaceBonus: 0,
        FunBonus: 0,
        KonjouBonus: 0,
        InitialKonjou: 0,
        skillPT: 0,
        other: '',
        staminaUP: 20,
        konjouUP: 9,
        DistanceType: '中距離',
        RaceType: '先行差し',
      },
      {
        name: 'sp_149.png',
        GoodAtBonus: 46,
        FriendBonus: 28,
        MotivationBonus: 45,
        TrainingBonus: 0,
        StaminaBonus: 0,
        HintLV: 2,
        HintBonus: 30,
        InitialKizuna: 28,
        InitialStamina: 20,
        RaceBonus: 5,
        FunBonus: 0,
        KonjouBonus: 0,
        InitialKonjou: 0,
        skillPT: 0,
        other: '',
        staminaUP: 19,
        konjouUP: 8,
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
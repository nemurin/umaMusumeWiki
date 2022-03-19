<template>
<div>
  <Header /> 

<div>
  <h1>チャンミ</h1>
  <div>検索：<input type="text" v-model="search"></div>
  <div>検索距離：<input type="text" v-model="search_kyori"></div>
  <div>検索作戦：<input type="text" v-model="search_sakusen"></div>
       <table>
  <tbody v-for="skill in search_users"
       :key="skill.name" class="condition">
    <tr>
      <th class="select1">
        <img v-bind:src=skill.image>
        </th>
      <td>{{skill.name}}</td>
      <td>{{skill.cardType}}</td>
      <td>{{skill.basyo}}</td>
      <td>{{skill.kyori}}</td>
      <td>{{skill.sakusen}}</td>
      <td>{{skill.place}}</td>
      <td>{{skill.kaihuku}}</td>
      <td>{{skill.passive}}</td>
      <td>{{skill.time}}</td>
      <td>{{skill.speed}}</td>
      <td>{{skill.acceleration}}</td>
      <td>{{skill.cooldown}}</td>
      <td>{{skill.point}}</td>
      <td><img v-bind:src=skill.howto></td>
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
      search:'',
      search_kyori:'',
      search_sakusen:'',
      skills: [
        {
        image: 'koyuu.png',
        cardType: 'タイプ',
        name: '名前',
        basyo: '場所',
        kyori: '距離',
        sakusen: '作戦',
        place: '順位位置',
        speed: '目標速度',
        acceleration: '目標加速度',
        kaihuku: '回復量',
        passive: 'パッシブ',
        time: '有効時間',
        cooldown: 'クール',
        point: 'ポイント',
        howto: '',
      },
        {
        image: 'koyuu.png',
        name: '白い稲妻、見せたるで！(継承)',
        cardType: '速度加速度',
        basyo: '中盤50%以降',
        kyori: '',
        sakusen: '先行、追込',
        place: '20-30%,70-75%',
        speed: '0.15',
        acceleration: '0.05',
        time: '3秒',
        cooldown: '500秒',
        point: '200pt',
        howto: 'i_61.png',
      },
      {
        image: 'healing.png',
        name: '後方待機',
        cardType: '回復',
        basyo: '中盤',
        kyori: '',
        sakusen: '追込',
        place: '75%以降',
        speed: '',
        acceleration: '',
        kaihuku: '1.5%',
        time: '',
        cooldown: '500秒',
        point: '180pt',
        howto: '',
      },
      {
        image: 'koyuu.png',
        name: '汝、皇帝の神威を見よ(継承)',
        cardType: '速度',
        basyo: '終盤',
        kyori: '',
        sakusen: '差し追込',
        place: '3回追い抜く',
        speed: '0.25',
        acceleration: '',
        kaihuku: '',
        time: '3秒',
        cooldown: '500秒',
        point: '180pt',
        howto: 'i_8.png',
      },
      {
        image: 'rarespeed.png',
        name: '弧線のプロフェッサー',
        cardType: '金速度',
        basyo: 'コーナー',
        kyori: '',
        sakusen: '',
        place: '',
        speed: '0.35',
        acceleration: '',
        kaihuku: '',
        time: '2.4秒',
        cooldown: '30秒',
        point: '180pt',
        howto: 'sp_108.png',
      },
      {
        image: 'healing.png',
        name: '円弧のマエストロ',
        cardType: '金回復',
        basyo: 'コーナー',
        kyori: '',
        sakusen: '',
        place: '',
        speed: '',
        acceleration: '',
        kaihuku: '5.5%',
        time: '',
        cooldown: '500秒',
        point: '170pt',
        howto: 'sp_16.png',
      },
      {
        image: 'koyuu.png',
        name: '直線一気',
        cardType: '加速',
        basyo: '終盤',
        kyori: '',
        sakusen: '追込',
        place: '追込',
        speed: '',
        acceleration: '0.2',
        kaihuku: '',
        time: '0.9s',
        cooldown: '500秒',
        point: '180pt',
        howto: '',
      },
      {
        image: 'koyuu.png',
        name: '内弁慶',
        cardType: '速度',
        basyo: '最終コーナー',
        kyori: '長距離',
        sakusen: '',
        place: '',
        speed: '0.15',
        acceleration: '',
        kaihuku: '',
        time: '3秒',
        cooldown: '500秒',
        point: '160pt',
        howto: '',
      },
      {
        image: 'koyuu.png',
        name: '長距離コーナー',
        cardType: '速度',
        basyo: 'コーナー',
        kyori: '長距離',
        sakusen: '',
        place: '',
        speed: '0.15',
        acceleration: '',
        kaihuku: '',
        time: '3秒',
        cooldown: '500秒',
        point: '100pt',
        howto: '',
      },
      {
        image: 'koyuu.png',
        name: '追込直線',
        cardType: '速度',
        basyo: '直線',
        kyori: '',
        sakusen: '追込',
        place: '',
        speed: '0.15',
        acceleration: '',
        kaihuku: '',
        time: '3秒',
        cooldown: '500秒',
        point: '130pt',
        howto: '',
      },
      {
        image: 'healing.png',
        name: '冷静',
        cardType: '回復',
        basyo: 'ブロック1秒',
        kyori: '',
        sakusen: '追込',
        place: '',
        speed: '',
        acceleration: '',
        kaihuku: '',
        passive: '賢さ40視野5m',
        time: '',
        cooldown: '500秒',
        point: '180pt',
        howto: '',
      },
      {
        image: 'passive_kasikosa.png',
        name: '追い込みのコツ',
        cardType: 'パッシブ',
        basyo: '',
        kyori: '',
        sakusen: '追込',
        place: '',
        speed: '',
        acceleration: '',
        kaihuku: '',
        time: '',
        cooldown: '500秒',
        point: '180pt',
        howto: '',
      },
      {
        image: 'koyuu.png',
        name: '一番星',
        cardType: '速度加速度回復',
        basyo: '中盤50%以降',
        kyori: '',
        sakusen: '',
        place: '',
        speed: '0.3',
        acceleration: '0.36',
        kaihuku: '4.2%',
        time: '1.2秒',
        cooldown: '500秒',
        point: '200pt',
        howto: '',
      },

      {
        image: 'koyuu.png',
        name: '追い込みコーナー',
        cardType: '速度',
        basyo: 'コーナー',
        kyori: '',
        sakusen: '追込',
        place: '',
        speed: '0.15',
        acceleration: '0',
        kaihuku: '',
        time: '3秒',
        cooldown: '500秒',
        point: '130pt',
        howto: '',
      },
      {
        image: 'koyuu.png',
        name: '絶対は、ボクだ(継承)',
        cardType: '速度',
        basyo: '最終コーナー以降',
        kyori: '',
        sakusen: '',
        place: '50%より上位2秒追い越し',
        speed: '0.25',
        acceleration: '',
        kaihuku: '',
        time: '3秒',
        cooldown: '500秒',
        point: '200pt',
        howto: '',
      },
      {
        image: 'healing.png',
        name: '直線回復',
        cardType: '回復',
        basyo: '直線',
        kyori: '',
        sakusen: '',
        place: '',
        speed: '',
        acceleration: '',
        kaihuku: '1.5%',
        time: '',
        cooldown: '500秒',
        point: '170pt',
        howto: '',
      },
      {
        image: 'healing.png',
        name: '下校の楽しみ',
        cardType: '回復',
        basyo: '下り坂',
        kyori: '',
        sakusen: '',
        place: '',
        speed: '',
        acceleration: '',
        kaihuku: '1.5%',
        time: '',
        cooldown: '500秒',
        point: '170pt',
        howto: '',
      },
      {
        image: 'koyuu.png',
        name: '勝ち関ワッショイ',
        cardType: '速度加速度',
        basyo: '第三コーナー2位以内/終盤',
        kyori: '',
        sakusen: '',
        place: '',
        speed: '0.05',
        acceleration: '0.1',
        kaihuku: '',
        time: '3秒',
        cooldown: '500秒',
        point: '200pt',
        howto: '',
      },
      {
        image: 'healing.png',
        name: '下校後のスペシャリスト',
        cardType: '金回復',
        basyo: '下り坂',
        kyori: '',
        sakusen: '',
        place: '',
        speed: '',
        acceleration: '',
        kaihuku: '5.5%',
        time: '',
        cooldown: '500秒',
        point: '170pt',
        howto: '',
      },
      {
        image: 'debahu_sokudo.png',
        name: 'まなざし',
        cardType: '速度デバフ',
        basyo: '終盤2位以降',
        kyori: '',
        sakusen: '追込',
        place: '',
        speed: '-0.15',
        acceleration: '',
        kaihuku: '',
        time: '3秒',
        cooldown: '500秒',
        point: '180pt',
        howto: '',
      },
      {
        image: 'koyuu.png',
        name: '追い上げ',
        cardType: '速度',
        basyo: '終盤',
        kyori: '長距離',
        sakusen: '',
        place: '',
        speed: '0.15',
        acceleration: '',
        kaihuku: '',
        time: '3秒',
        cooldown: '500秒',
        point: '160pt',
        howto: '',
      },
      {
        image: 'koyuu.png',
        name: 'コーナー巧者',
        cardType: '速度',
        basyo: 'コーナー',
        kyori: '',
        sakusen: '',
        place: '',
        speed: '0.15',
        acceleration: '',
        kaihuku: '',
        time: '2.4秒',
        cooldown: '30秒',
        point: '180pt',
        howto: '',
      },
      {
        image: 'koyuu.png',
        name: '仕掛け抜群',
        cardType: '速度',
        basyo: '終盤',
        kyori: '',
        sakusen: '追込',
        place: '上位50%以降',
        speed: '0.15',
        acceleration: '',
        kaihuku: '',
        time: '3秒',
        cooldown: '500秒',
        point: '180pt',
        howto: '',
      },
      {
        image: 'koyuu.png',
        name: '阪神レース場',
        cardType: '速度加速度回復',
        basyo: '中盤50%以降',
        kyori: '',
        sakusen: '',
        place: '',
        speed: '0.3',
        acceleration: '0.36',
        kaihuku: '4.2%',
        time: '1.2秒',
        cooldown: '500秒',
        point: '200pt',
        howto: '',
      },
      
      
      
     ],
  }
  },
   computed: {
        search_users(){

        let searchWord = this.search;

        return this.skills.filter(skills => {
            return skills.cardType.includes(searchWord)
            && (skills.kyori.includes(this.search_kyori)
            || skills.sakusen.includes(this.search_sakusen))
            ;
        })
        }
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
<template>
	<ul>
    <li class="selection"><router-link to="/">index</router-link></li>
    <li class="selection"><router-link to="/mejiroRian">メジロライアン</router-link></li>
    <li class="selection"><router-link to="/smartFarcon">スマートファルコン</router-link></li>
    <li class="selection"><router-link to="/capricorn">カプリコーン杯</router-link></li>
    <li class="selection"><router-link to="/erucondorupasar">エルコンドルパサー</router-link></li>
    <li class="selection"><router-link to="/ogriCap">オグリ</router-link></li>
  </ul>
</template>
<script>
	export default {
		components: {}
	};
</script>
<style>
li.selection {
    list-style: none;
    top: 50%;
    margin-top: -10px;
    content: '';
    border-left: 1px solid #f2f2f2;
    position: relative;
    display: block;
    float: left;
    width: 109px;
    height: 12px;
    font-size: 12px;
    text-align: center;
    cursor: pointer;
}
</style>
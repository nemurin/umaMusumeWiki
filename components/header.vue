<template>
	<ul>
    <li class="selection"><router-link to="/">index</router-link></li>
    <li class="selection"><router-link to="/other">other</router-link></li>
    <li class="selection"><router-link to="/sample">sample</router-link></li>
  </ul>
</template>
<script>
	export default {
		components: {}
	};
</script>
<style>
li {
    list-style: none;
}
</style>
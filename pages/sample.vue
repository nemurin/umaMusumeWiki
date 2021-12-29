<template>
 <div class="page">
   <Header />
   <ul>
     <li
       v-for="item in items"
       :key="item.message"
     >
       {{ item.message }}
     </li>
   </ul>
 </div>
</template>
<style>
body {
    margin: 0;
    padding: 0;
    color: #444;
    font-size: 14px;
    font-family: Hiragino Kaku Gothic Pro,"ヒラギノ角ゴ Pro W3",Meiryo,"メイリオ",Osaka,MS PGothic,arial,helvetica,sans-serif;
    line-height: 1.6;
    background: #FFF;
}
li {
    list-style: none;
}

h4 {  
    padding: 5px 0 5px 30px;
    background-size: 25px 25px;
    color: inherit;
    background-repeat: no-repeat;
    background-position: left center;
    margin: 15px 0 10px;
    display: block;
    margin-block-start: 1.33em;
    margin-block-end: 0.33em;
    margin-inline-start: 0px;
    margin-inline-end: 0px;
    font-weight: bold;
}
tbody {
    display: table-row-group;
    vertical-align: middle;
    border-color: inherit;
}
table tr th {
    border: 1px solid #B1CEA6;
    background-color: #F5FCF2;
}
table tr td {
    border: 1px solid #B1CEA6;
    background-color: #FFF;
}
td {
    display: table-cell;
    vertical-align: inherit;
}
table {
    border-collapse: collapse;
    border-spacing: 0;
}
.select1{
    background-color: #dcedc8!important;;
}
.select2{
    background-color: #fff9c4!important;
}
</style>
<script>
export default {
 data () {
   return {
     items: [
       { message: 'Foo' },
       { message: 'Bar' },
     ]
   }
 },
}
</script>
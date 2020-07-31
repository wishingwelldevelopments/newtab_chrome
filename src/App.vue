<template>
	<div class="quote">
		<h1>{{ quote.quote }}</h1>
		<p>{{ quote.name }}</p>
	</div>
</template>

<script>
import json from './assets/quotes.json'

export default {
  name: 'App',
	data(){
		return{
			quotes:json,
			quote:[]
		}
	},
	created(){
		const i = Math.floor(Math.random() * this.quotes.length);
		this.quote = this.quotes[i];
	}
}
</script>
<style>
@font-face {
  font-family: 'quote';
	src:  url('./assets/font.woff2') format('woff2');
}
*{
	margin:0px;
	padding:0px;
}
body{
	background-color:#ececec;
	display:flex;
	width:100%;
	height:100vh;
	justify-content:center;
	align-items:center;
	flex-direction:column;
	text-align:center;
}
p{
	color:grey;
	font-size:20px;
	font-family: Cantarell, Arial, sans-serif;
	text-transform:uppercase;
	font-weight:bold;
}
h1{
	width:460px;
	color:#2b2b2b;
	font-family: "quote", Arial, sans-serif;
	margin-bottom:30px;
	font-size:40px;
}
</style>

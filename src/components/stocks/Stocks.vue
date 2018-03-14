<template>
	<div class="row">
		<app-stock v-for="stock in stocks" :stock="stock"> </app-stock>
	</div>
</template>
<script>
import Stock from './Stock.vue'; 

export default {
	components:{
		appStock: Stock,
	},
	data(){
		return {
			stocks: [
				{
					id: 1,
					name: "BMW",
					price: 110,
				},
				{
					id: 2,
					name: "Google",
					price: 10,
				},
				{
					id: 3,
					name: "Twitter",
					price: 2,
				},
			],
		};
	},
};

</script>
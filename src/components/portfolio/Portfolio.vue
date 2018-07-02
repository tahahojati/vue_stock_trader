<template>
	<div class="col-sm-6 col-md-4">
	</div>
</template>

<script>
import {mapGetters} from 'vuex';
import Stock from './Stock.vue';


export default {
	computed:{
		...mapGetters({
			stocks: 'stockPortfolio'
		})
	},
	components: {
		appStock: Stock,
	}
};
</script>

<template>
	<div class="col-sm-6 col-md-4">
		<div class="panel panel-success">
			<div class="panel-heading">
				<h3 class="panel-title"> 
					{{stock.name}}
					<small>(Price: {{stock.price}})</small> 
				</h3>
			</div>
			<div class="panel-body">
				<div class="pull-left">
					<input v-model.number="quantity" type ="number" class="form-control" placeholder="Quantity" />
				</div>
				<div class="pull-right">
					<button class="btn btn-success" @click="buyStock" :disabled="quantity <= 0 || !Number.isInteger(quantity)"> Buy </button>
				</div>
			</div>
		</div>
	</div>
</template>
<script>
export default {
	props:["stock"],
	data(){
		return {
			quantity: null ,

		};
	},
	methods: {
		buyStock(){
			const order = {
				stockId: this.stock.id,
				stockPrice: this.stock.price,
				quantity: this.quantity
			};
			console.log("order placed: ",order);
			this.quantity = null ;
		}
	},
	filters: {
		to_int: {
			read(value){
				return floor(value);
			},
			write(value){
				return floor(value);
			},
		},
	},
};
</script>
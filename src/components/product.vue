<template>
	<div class="hd">
		<!-- Standard button -->
		<button type="button" class="btn btn-primary">报名商品</button>
		<span>活动商品</span>
		<table class="table table-striped">
			<thead>
				<tr>
					<th>商品</th>
					<th>标题</th>
					<th>库存</th>
					<th>总销量</th>
					<th>销售模式</th>
					<th>报名时间</th>
					<th>状态</th>
					<th>操作</th>
				</tr>
			</thead>
			<tbody>
				<tr v-for="list in products">
					
					<td>
						<img src="../assets/images/tb1.png">
					</td>
					<td class="tit">{{list.tit}}</td>
					<td>{{list.all}}</td>
					<td>{{list.num}}</td>
					<td>{{list.type}}</td>
					<td>{{list.time}}</td>
					<td >
						<span v-if='list.status==1'>全款</span>
						<span v-if='list.status==2'>订金</span>
						<span v-if='list.status==3'>特权订金</span>

					</td>
					<td></td>
					
				</tr>
				
			</tbody>
		</table>

	</div>
</template>
<script>
    export default {
        replace:true,
        props: ['products'],
        methods:{

        }
    }
</script>
<style lang="sass">
	.main {
		margin-left:180px;
		.hd {
			margin-top: 10px;
		}
	}
	table.table-striped {
		width:auto;
		.tit {
			width:300px;
		}
	}
</style>
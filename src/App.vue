<template>

	<div class="common-layout">
	<el-container>
		<el-header>
			<el-menu mode="horizontal" id="nav" @select="handleSelect">
				<el-menu-item index="/">Profile</el-menu-item>
				<el-sub-menu index="/tools">
					<template #title>
						Tools
					</template>
					<el-menu-item index="/tools/jwt">JWT</el-menu-item>
				</el-sub-menu>
			</el-menu>
		</el-header>
		<el-main>
			<router-view />
		</el-main>
	</el-container>
	</div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
	name:"App",
	methods:{
		handleSelect : function (index:string) {
			this.$router.push(index)
		}
	}
})


</script>

<style>
</style>

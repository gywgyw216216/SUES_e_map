<template>
	<div>
	<router-view></router-view>
	<div id="footer">
		<p id="copyright">
			© 2020-{{year}} SUES All Rights Reserved. Version 0.1<br><a href="https://www.beian.miit.gov.cn" target="_blank">-----</a>
		</p>
	</div>
	</div>
</template>

<script>
export default{
	data() {
		return {
			year:'',
			getda:false
		};
	},
	mounted() {
		this.getCurrentYear()
		console.log("Developed By DexterCai %c (i@dextercai.com)","color:red")
	},
	methods: {
		getCurrentYear() {
			let date = new Date();
			let y = date.getFullYear();
			this.year = y;

		}
	}
}
</script>

<style>
	#app {
		font-family: 'Avenir', Helvetica, Arial, sans-serif;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
		text-align: center;
		color: #2c3e50;
		margin-top: 60px;
	}
	div #footer {
		background: #303030;
		font-family: 'Avenir', Helvetica, Arial, sans-serif;
		text-align: center;
	}
	#copyright {
		color: #ffffff;
		padding: 5px 0px;
	}
	#copyright a {
		color: #28a7e9;
		font-weight: bold;
	}
</style>

<template>
    <el-row :gutter="68">
			<el-carousel :interval="0" arrow="never" height="600px" type="card" class="intro">
				<el-carousel-item v-for="item in dataimg" :key="item">
					<div class="grid-content">
						<el-col :span="12">
							<div class="box">
								<img :src="item.src">
							</div>
						</el-col>
					</div>
				</el-carousel-item>
			</el-carousel>
		</el-row>
</template>
<script>
export default {
		name: 'marketAnalysis',
		data() {
			return {
				
				dataimg: [
					{
						src: require('./img/1.jpg')
					},
					{
						src: require('./img/2.jpg')
					},
					{
						src: require('./img/3.jpg')
					},
					{
						src: require('./img/4.jpg')
					},
					{
						src: require('./img/5.jpg')
					},
					{
						src: require('./img/6.jpg')
					},
					{
						src: require('./img/7.jpg')
					},
					{
						src: require('./img/8.jpg')
					},
					{
						src: require('./img/9.jpg')
					},
					{
						src: require('./img/10.jpg')
					},
					{
						src: require('./img/11.jpg')
					}
				]
			}
		}
	}
</script>
<style>
  .intro {
	  background-image: url("./img/bk.jpg");
	  background-size: 100%;
  }
  .box {
    align-items: center;
  }
  .box img {
    width: 240%;
  }
</style>
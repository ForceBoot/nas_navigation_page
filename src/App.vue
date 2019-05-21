<template>
	<div id="app">
		<particles class="particles" />
		<div class="container">
			<div class="top">
				<a-row>
					<a-col :span="12"
					       :offset="6">
						<icon-font type="iconcloudlogo"
						           class="TOPICON" />
						<span class="TOPTITLE">
							WELCOME
						</span>
					</a-col>
				</a-row>
			</div>
			<a-row>
				<a-col :span="12"
				       :offset="6">
					<a-list :grid="{ gutter: 16, xs: 2, sm: 2, md: 4, lg: 4, xl: 4, xxl: 4 }"
					        :dataSource="data">
						<a-list-item class="lists"
						             slot="renderItem"
						             slot-scope="item, index">
							<a :href="item.href"
							   target="_blank">
								<icon-font :type="item.type"
								           class="icon shake" />
								<span class="title">
									{{item.title}}
								</span></a>
						</a-list-item>
					</a-list>
				</a-col>
			</a-row>
		</div>
	</div>
</template>

<script>
import particles from "./components/particles";
import { Icon } from 'ant-design-vue';

const IconFont = Icon.createFromIconfontCN({
	scriptUrl: '//at.alicdn.com/t/font_1201034_mfll8gpu7h.js',
})
const data = [
	{
		title: 'IKUAI',
		type: 'iconluyou1',
		href: 'http://home.addxx.com:5002'
	},
	{
		title: 'LEDE',
		type: 'iconluyouqi',
		href: 'http://home.addxx.com:5004'
	},
	{
		title: 'AC88U',
		type: 'iconluyou',
		href: 'http://home.addxx.com:5003'
	},
	{
		title: 'NAS SYSTEM',
		type: 'iconnas',
		href: 'http://nas.addxx.com:5000'
	},
	{
		title: 'MOVIE',
		type: 'iconmovie',
		href: 'http://nas.addxx.com:5000/?launchApp=SYNO.SDS.VideoStation.AppInstance#!Home'
	},
	{
		title: 'CLOUD DISK',
		type: 'iconclouddisk',
		href: 'http://nas.addxx.com:5000/?launchApp=SYNO.SDS.Drive.Application'
	},
	{
		title: 'PHOTO',
		type: 'iconxiangce',
		href: 'http://nas.addxx.com:8085/photo/#!Albums'
	}
	, {
		title: 'PROXMOX VE',
		type: 'iconvmware',
		href: 'https://home.addxx.com:5001'
	}
]
export default {
	name: 'app',
	data () {
		return {
			data
		}
	},
	components: {
		particles,
		IconFont
	},
	created () {
		document.title = 'Home'
	}
}
</script>

<style lang="scss">
body {
	overflow: hidden;
	width: 100%;
	height: 100%;
	font-size: 100%;
	background: -webkit-linear-gradient(315deg, #00c4ff, #9d1bb2) no-repeat
		fixed;
	background: linear-gradient(135deg, #00c4ff, #9d1bb2) no-repeat fixed;
	overflow: hidden;
	font-family: "Helvetica Neue", "Microsoft Yahei", SimHei, sans-serif;
}
#app {
	width: 100%;
	height: 100%;
}
.particles {
	width: 100%;
	height: 100%;
	position: absolute;
}
.container {
	width: 100%;
	height: 100%;
	position: absolute;
}
.top {
	margin-top: 10%;
	text-align: center;
	.TOPICON {
		font-size: 10rem;
		color: #fff;
	}
	.TOPTITLE {
		color: #fff;
		font-size: 18px;
		display: block;
		text-align: center;
	}
}
.lists {
	text-align: center;
	color: #fff;
	a {
		cursor: pointer;
		color: #fff;
	}
	padding-top: 20px;
	.title {
		display: block;
		font-size: 16px;
		padding-top: 20px;
	}
	.icon {
		font-size: 36px;
		width: 96px;
		height: 96px;
		line-height: 96px;
		border: 2px solid #fff;
		border-radius: 50%;
	}
	@-webkit-keyframes shake {
		0%,
		100% {
			-webkit-transform: translateX(0);
			transform: translateX(0);
		}

		10%,
		30%,
		50%,
		70%,
		90% {
			-webkit-transform: translateX(-10px);
			transform: translateX(-10px);
		}

		20%,
		40%,
		60%,
		80% {
			-webkit-transform: translateX(10px);
			transform: translateX(10px);
		}
	}
}
@keyframes shake-bounce {
	0%,
	100% {
		-webkit-transform: rotate(0);
		-moz-transform: rotate(0);
		transform: rotate(0);
		-ms-transform: rotate(0);
	}

	25% {
		-webkit-transform: rotate(15deg);
		-moz-transform: rotate(15deg);
		transform: rotate(15deg);
		-ms-transform: rotate(15deg);
	}

	50% {
		-webkit-transform: rotate(-15deg);
		-moz-transform: rotate(-15deg);
		transform: rotate(-15deg);
		-ms-transform: rotate(-15deg);
	}

	75% {
		-webkit-transform: rotate(5deg);
		-moz-transform: rotate(5deg);
		transform: rotate(5deg);
		-ms-transform: rotate(5deg);
	}

	85% {
		-webkit-transform: rotate(-5deg);
		-moz-transform: rotate(-5deg);
		transform: rotate(-5deg);
		-ms-transform: rotate(-5deg);
	}
}

@-webkit-keyframes shake-bounce {
	0%,
	100% {
		-webkit-transform: rotate(0);
		-moz-transform: rotate(0);
		transform: rotate(0);
		-ms-transform: rotate(0);
	}

	25% {
		-webkit-transform: rotate(15deg);
		-moz-transform: rotate(15deg);
		transform: rotate(15deg);
		-ms-transform: rotate(15deg);
	}

	50% {
		-webkit-transform: rotate(-15deg);
		-moz-transform: rotate(-15deg);
		transform: rotate(-15deg);
		-ms-transform: rotate(-15deg);
	}

	75% {
		-webkit-transform: rotate(5deg);
		-moz-transform: rotate(5deg);
		transform: rotate(5deg);
		-ms-transform: rotate(5deg);
	}

	85% {
		-webkit-transform: rotate(-5deg);
		-moz-transform: rotate(-5deg);
		transform: rotate(-5deg);
		-ms-transform: rotate(-5deg);
	}
}

@-moz-keyframes shake-bounce {
	0%,
	100% {
		-webkit-transform: rotate(0);
		-moz-transform: rotate(0);
		transform: rotate(0);
		-ms-transform: rotate(0);
	}

	25% {
		-webkit-transform: rotate(15deg);
		-moz-transform: rotate(15deg);
		transform: rotate(15deg);
		-ms-transform: rotate(15deg);
	}

	50% {
		-webkit-transform: rotate(-15deg);
		-moz-transform: rotate(-15deg);
		transform: rotate(-15deg);
		-ms-transform: rotate(-15deg);
	}

	75% {
		-webkit-transform: rotate(5deg);
		-moz-transform: rotate(5deg);
		transform: rotate(5deg);
		-ms-transform: rotate(5deg);
	}

	85% {
		-webkit-transform: rotate(-5deg);
		-moz-transform: rotate(-5deg);
		transform: rotate(-5deg);
		-ms-transform: rotate(-5deg);
	}
}

@-o-keyframes shake-bounce {
	0%,
	100% {
		-webkit-transform: rotate(0);
		-moz-transform: rotate(0);
		transform: rotate(0);
		-ms-transform: rotate(0);
	}

	25% {
		-webkit-transform: rotate(15deg);
		-moz-transform: rotate(15deg);
		transform: rotate(15deg);
		-ms-transform: rotate(15deg);
	}

	50% {
		-webkit-transform: rotate(-15deg);
		-moz-transform: rotate(-15deg);
		transform: rotate(-15deg);
		-ms-transform: rotate(-15deg);
	}

	75% {
		-webkit-transform: rotate(5deg);
		-moz-transform: rotate(5deg);
		transform: rotate(5deg);
		-ms-transform: rotate(5deg);
	}

	85% {
		-webkit-transform: rotate(-5deg);
		-moz-transform: rotate(-5deg);
		transform: rotate(-5deg);
		-ms-transform: rotate(-5deg);
	}
}

.shake:hover {
	-webkit-animation: shake-bounce 0.5s alternate;
	-moz-animation: shake-bounce 0.5s alternate;
	-o-animation: shake-bounce 0.5s alternate;
	animation: shake-bounce 0.5s alternate;
}
</style>

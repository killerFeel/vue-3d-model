<template>
	<div id="exp">
		<!-- 3D模型集成 -->
		<model-fbx :backgroundColor="'#454e52'" :lights="lights" :backgroundAlpha="0.5" src="/models/tree/tree_01.fbx">
		</model-fbx>
	</div>
</template>

<script>
	import {
		ModelFbx
	} from '@/vue-3d-model';

	export default {
		name: "exp",
		components: {
			ModelFbx
		},
		data() {
			return {
				lights: [{
					type: 'HemisphereLight',
					position: {
						x: 0,
						y: 1,
						z: 0
					},
					skyColor: 0xffffff,
					// groundColor: 0xFF0000, 此代码为灯光后颜色
					intensity: 1,
				}, {
					type: 'DirectionalLight',
					position: {
						x: 1,
						y: 1,
						z: 1
					},
					color: 0xffffff,
					intensity: .8,
				}],
			}
		}
	}
</script>

<style scoped>

</style>

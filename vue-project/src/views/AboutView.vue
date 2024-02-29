<template>
  <div>
    <canvas ref="canvas" />
  </div>
</template>

<script setup>
import * as THREE from 'three';
import { GLTFLoader } from 'three/addons/loaders/GLTFLoader.js';
import { OrbitControls } from 'three/addons/controls/OrbitControls.js';

console.log(THREE);
const scene = new THREE.Scene();
const camera = new THREE.PerspectiveCamera( 75, window.innerWidth / window.innerHeight, 0.001, 1000 );

const renderer = new THREE.WebGLRenderer({alpha: true});
renderer.setSize( window.innerWidth, window.innerHeight );
document.body.appendChild( renderer.domElement );

const light = new THREE.AmbientLight( 0x404040, 100 );
scene.add( light );

const controls = new OrbitControls( camera, renderer.domElement );
camera.position.set( -10, 0, 0 ,);
controls.update();
controls.autoRotate = true;
controls.autoRotateSpeed = 2.0;


camera.position.z = 5;

const loader = new GLTFLoader();


loader.load(

	'./5_3_2023.glb',

	function ( gltf ) {
		const model = gltf.scene
		scene.add( gltf.scene );
		gltf.animations; 
		gltf.scene; 
		gltf.scenes; 
		gltf.cameras; 
		gltf.asset; 

	},
	
	function ( xhr ) {

		console.log( ( xhr.loaded / xhr.total * 100 ) + '% loaded' );

	},
	
  function (error) {
    console.error(error);
}

);

function animate(model) {
    requestAnimationFrame( animate );

	if (model) {
		model.rotation.x += 0.01
	}

	controls.update

    renderer.render( scene, camera );
}
animate();

</script>

<style scoped>
canvas {
  width: 100%;
  height: 100%;
  display: block;
}
</style>

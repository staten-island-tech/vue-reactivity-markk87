<template>
  <div>
    <canvas ref="canvas" />
  </div>
</template>

<script>
import * as THREE from 'three';
import { GLTFLoader } from 'three/addons/loaders/GLTFLoader.js';

console.log(THREE);
const scene = new THREE.Scene();
const camera = new THREE.PerspectiveCamera( 75, window.innerWidth / window.innerHeight, 0.1, 1000 );

const renderer = new THREE.WebGLRenderer();
renderer.setSize( window.innerWidth, window.innerHeight );
document.body.appendChild( renderer.domElement );



camera.position.z = 5;

const loader = new GLTFLoader();


loader.load(

	'@assets/brandon.glb',

	function ( gltf ) {

		scene.add( gltf.scene );

		gltf.animations; 
		gltf.scene; 
		gltf.scenes; 
		gltf.cameras; 
		gltf.asset; 

	},
	// called while loading is progressing
	function ( xhr ) {

		console.log( ( xhr.loaded / xhr.total * 100 ) + '% loaded' );

	},
	// called when loading has errors
  function (error) {
    console.error(error);
}

);

function animate() {
    requestAnimationFrame( animate );
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

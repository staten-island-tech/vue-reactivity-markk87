<template>
  <div>
    <canvas ref="canvas" />
  </div>
</template>

<script>
import * as THREE from 'three';
import { GLTFLoader } from 'three/examples/jsm/loaders/GLTFLoader.js';

export default {
  mounted() {
    const scene = new THREE.Scene();
    const camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);

    const renderer = new THREE.WebGLRenderer({ antialias: true });
    renderer.setSize(window.innerWidth, window.innerHeight);
    this.$refs.canvas.appendChild(renderer.domElement);

    const loader = new GLTFLoader();


    loader.load('@/assets/3D_Model/scene.gltf', function (gltf) {
      scene.add(gltf.scene);
    }, undefined, function (error) {
      console.error(error);
    });

    camera.position.z = 5;

    function animate() {
      requestAnimationFrame(animate);
      renderer.render(scene, camera);
    }

    animate();
  }
};
</script>

<style scoped>
canvas {
  width: 100%;
  height: 100%;
  display: block;
}
</style>

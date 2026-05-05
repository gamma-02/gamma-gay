<script>
    import { Canvas } from '@threlte/core'
    import Scene from './3d-test/Scene.svelte'
    import { AsciiRenderer } from '@threlte/extras'


</script>

<div class="container-box">
    <div class="vertical-grid">
        <h1> 404 Not Found! </h1>

        <div style="width: 500px; height: 500px; border: 5px solid black;">
            <Canvas colorSpace="srgb">
                <AsciiRenderer characters=" .:-+*=%@#" options={{ color: false }} fgColor="#d43939"/>
                <Scene />
            </Canvas>
        </div>
<!--        <p>hi!</p>-->
    </div>
</div>
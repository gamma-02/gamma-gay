<script>
    import { Canvas } from '@threlte/core'
    import Scene from './3d-test/Scene.svelte'
    import { AsciiRenderer } from '@threlte/extras'


</script>

<div class="container-box">
    <div class="vertical-grid">
        <h1> 404 Not Found! </h1>

        <div style="width: 400px; height: 400px; border: 5px solid black;">
            <Canvas colorSpace="srgb">
                <AsciiRenderer />
                <Scene />
            </Canvas>
        </div>
<!--        <p>hi!</p>-->
    </div>
</div>
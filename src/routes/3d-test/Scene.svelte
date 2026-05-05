<script>

    let { scaleWithMouseOver = true, ...props } = $props();

    import {T, useTask} from '@threlte/core'
    import { interactivity } from '@threlte/extras'
    import { Spring } from 'svelte/motion'
    import Teapot from './teapot.svelte'

    interactivity()
    const scale = new Spring(2)

    let rotation = $state(0)
    useTask((delta) => {
        rotation += delta
    })

    // let mouseRotation = $state({x:0, y:0});
    // document.addEventListener('mousemove', (event) => {
    //     // Normalize mouse coordinates to -1 to +1
    //     const mouseX = (event.clientX / window.innerWidth) * 2 - 1;
    //     const mouseY = -(event.clientY / window.innerHeight) * 2 + 1;
    //
    //     // Rotate object based on movement
    //     mouseRotation.y = mouseX * Math.PI; // Horizontal moves rotate Y
    //     mouseRotation.x = mouseY * Math.PI; // Vertical moves rotate X
    //
    // });



</script>

<T.PerspectiveCamera
        makeDefault
        position={[10, 10, 10]}
        oncreate={(ref) => {
            ref.lookAt(0, 1, 0)
        }}
/>

<T.DirectionalLight position={[0, 10, 10]} color="#ffffff" />


<Teapot
        position.y={-2}
        rotation.y={rotation}
        scale={scale.current}

        onpointerenter={() => {
            if(scaleWithMouseOver)
                scale.target = 3.5
        }}
        onpointerleave={() => {
            if(scaleWithMouseOver)
                scale.target = 2
        }}

        fallback=""
        error=""
        children=""
/>

<!--<T.Mesh-->
<!--        rotation.x={-Math.PI / 2}-->
<!--        receiveShadow-->
<!--&gt;-->
<!--    <T.CircleGeometry args={[4, 40]} />-->
<!--    <T.MeshStandardMaterial color="white" />-->
<!--</T.Mesh>-->

<!--<T.Mesh position.y={1}-->
<!--        scale={scale.current}-->
<!--        onpointerenter={() => {-->
<!--            scale.target = 1.5-->
<!--        }}-->
<!--        onpointerleave={() => {-->
<!--            scale.target = 1-->
<!--        }}-->
<!--        castShadow-->

<!--&gt;-->
<!--    <T.BoxGeometry args={[1, 2, 1]} />-->
<!--    <T.MeshStandardMaterial color="hotpink" />-->
<!--</T.Mesh>-->
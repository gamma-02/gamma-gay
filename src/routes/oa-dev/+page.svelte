<script>
    let {width = "100%", height = "800px"} = $props()
</script>

<div class="unity-container">
    <iframe
            src="/Dev_10-21_web/web_build/index.html"
            title="Unity WebGL Build"
            style="width: {width}; height: {height};"
            frameborder="0"
            allow="autoplay; fullscreen; vr"
            allowfullscreen
    ></iframe>
</div>

<style>
    .unity-container {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 100%;
    }
</style>
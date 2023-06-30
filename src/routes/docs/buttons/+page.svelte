<script>
    export let exampleCodeHeader = "<button>Click Me!</button>";
</script>

<div class="page bg-dark">
    <section>
        <h1>Buttons</h1>
        <h2><code>{exampleCodeHeader}</code></h2>
    </section>

    <div class="list">
        <div class="flex">
            <button>Default</button>
            <button class="btn-invert">Inverted</button>
            <button class="btn-hollow">Hollow</button>
            <button class="btn-hollow-fill">Hollow filled</button>
        </div>
    </div>
</div>

<style>
    .flex {
        display: flex;
        justify-content: center;
        gap: 3rem;
    }
</style>
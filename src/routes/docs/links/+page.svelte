<script>
    export let ex = '<a href="#">Link</a>'
</script>

<div class="page bg-dark">
    <section>
        <h1>Links</h1>
        <h2><code>{ex}</code></h2>
    </section>

    <div class="list">
        <div class="flex">
            <a href="#">Link</a>
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
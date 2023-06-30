<div class="page">
    <aside>
        <nav class="bg-primary">
            <ul>
                <caption>Components</caption>
                <li><a href="/docs/buttons">Buttons</a></li>
                <li><a href="/docs/links">Links</a></li>
                <li><a href="/docs/dropdowns">Dropdowns</a></li>
                <caption>Customize</caption>
                <li><a href="/">wip</a></li>
                <li><a href="/">wip</a></li>
                <li><a href="/">wip</a></li>
                <li><a href="/">wip</a></li>
            </ul>
        </nav>
    </aside>
    <slot />
</div>

<style>
    .page {
        display: grid;
        grid-template-columns: 0.1fr 0.9fr;
        min-height: 100vh;
        min-height: 100dvh;
    }
    nav {
        min-height: 100vh;
        min-height: 100dvh;
    }
</style>
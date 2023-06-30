<script>
    let code = `
    @import url('https://fonts.googleapis.com/css2?family=Outfit&display=swap');

* {
    margin: 0;
    padding: 0;
    font-family: var(--ff-base);
}

p {
    font-size: var(--text-md);
}

body {
    background-color: var(--background-primary);
    color: var(--text-primary);
}

code {
    font-size: var(--text-md);
    background-color: var(--background-secondary);
    color: var(--text-secondary);
    font-weight: lighter;
    border-radius: 2px;
    padding-inline: 0.25em;
}

:root {
    --background-primary: rgb(52, 52, 52);
    --background-secondary: rgb(87, 87, 87);
    --background-dark: rgb(38, 38, 38);

    --text-primary: rgb(255, 255, 255);
    --text-secondary: rgb(203, 203, 203);
    --text-highlight: rgb(140, 140, 140);

    --button-primary: rgb(38, 38, 38);
    --button-primary-hover: gray;

    --ff-base: 'Outfit', sans-serif;

    --text-sm: 0.5rem;
    --text-md: 1.5rem;
    --text-lg: 2.5rem;
    --text-xl: 3.0rem;
}

/* utilities :) */
.bg-dark {
    background-color: var(--background-dark);
}
.bg-primary {
    background-color: var(--background-primary);
}
.bg-secondary {
    background-color: var(--background-secondary);
}
.text-sm {
    font-size: var(--text-sm);
}
.text-md {
    font-size: var(--text-md);
}
.text-lg {
    font-size: var(--text-lg);
}
.text-xl {
    font-size: var(--text-xl);
}

h1 {
    color: var(--text-primary);
    font-size: var(--text-lg);
}
h2 {
    color: var(--text-secondary);
    font-size: var(--text-md);
}

/* buttons !!! */
button {
    font-size: var(--text-md);
    padding: 0.5em;
    padding-inline: 1em;
    border-radius: 2em;
    background-color: var(--button-primary);
    color: var(--text-secondary);
    border: none;
    text-decoration: none;
    box-shadow: 0px 2px 2px 0px rgba(0, 0, 0, 0.25);

    transition: color 0.1s ease;
    transition: background-color 0.1s ease;
}
button:hover {
    cursor: pointer;
    filter: brightness(120%);
}
.btn-invert {
    color: var(--background-primary);
    background-color: var(--text-secondary);
}
.btn-hollow, .btn-hollow-fill {
    background: transparent;
    border-style: solid;
    border-color: var(--text-secondary);
}
.btn-hollow:hover {
    background-color: var(--background-primary);
}
.btn-hollow-fill:hover {
    filter: brightness(100%);
    background: var(--text-primary);
    color: var(--background-primary);
}
.btn-disabled {
    background-color: var(--background-secondary);
    color: var(--text-highlight);
    box-shadow: none;
}
.btn-disabled:hover {
    cursor: default;
    filter: brightness(100%);
    box-shadow: none;
}
.focus:focus {
    box-shadow: inset 0 0 0 3px var(--text-primary);
}
/* inputs !!! */


input, textarea {
    padding: 0.5em;
    padding-inline: 1em;
    border: none;
    outline: none;
    text-decoration: none;
    font-size: var(--text-md);
    border-radius: 2em;
    background-color: var(--background-secondary);
    color: var(--text-primary);
    caret-color: var(--text-secondary);
    box-shadow: 0px 2px 2px 0px rgba(0, 0, 0, 0.25);
}
input:focus, textarea:focus {
    box-shadow: inset 0 0 0 3px var(--text-primary);
}
input::placeholder {
    color: var(--text-secondary);
}
textarea {
    resize: none;
    padding: 1em;
}

/* links! */
a {
    text-decoration: none;
    color: var(--text-secondary);
    font-size: var(--text-md);
    transition: color 0.1s ease;
}
a:hover {
    color: var(--text-primary);
}

/* lists !!! */
ul {
    text-decoration: none;
    list-style: none;
    font-size: var(--text-md);
}

nav {
    display: flex;
    justify-content: space-between;
    background-color: var(--background-dark);
}
nav > ul {
    display: flex;
    align-items: center;
    gap: 1rem;
}
nav ul > li {
    margin: 0.5em;
}
nav ul:first-child li {
    font-weight: bold;
}
aside > nav > ul {
    display: flex;
    flex-direction: column;
    align-items: start;
}
aside > nav > ul > li {
    float: left;
}

/* dropdowns */

details {
    cursor: pointer;
    font-size: var(--text-md);
    background-color: var(--background-secondary);
    border-radius: 1em;
    position: relative;
    box-shadow: 0px 2px 3px 0px rgba(0, 0, 0, 0.25);
}
details[open] {
    border-radius: 1em 1em 0 0;
}
details > summary {
    list-style-type: none;
    padding: 0.5em;
    padding-inline: 1em;
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-direction: row-reverse;
}
details > summary > p {
    margin-right: 1em;
}
details summary::before {
    content: '+';
    float: right;
    font-size: var(--text-md);
}
details[open] summary::before {
    content: '-';
}
details ul {
    background-color: var(--background-primary);
    border-radius: 0 0 1em 1em;

    display: flex;
    flex-direction: column;
    box-shadow: 0px 2px 3px 0px rgba(0, 0, 0, 0.25);
}
details[open] ul {
    width: 100%;
    position: absolute;
    z-index: 1000;
}
.relative[open] ul {
    position: relative;
}
.relative[open] {
    border-radius: 1em;
}
details ul li {
    margin: 0.5em;
}

/* cards */
article {
    width: fit-content;
    background-color: var(--background-dark);
    font-size: var(--text-md);
    border-radius: 1em;
    box-shadow: 0px 2px 3px 0px rgba(0, 0, 0, 0.25);
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}
article > header, footer {
    background-color: var(--background-primary);
}
article * {
    padding: 1em;
}
/* header */
section {
    padding: 5rem;
    text-align: center;
}
section > h1 {
    font-size: var(--text-xl);
}
section button {
    margin: 1rem;
}
`
async function copyToClipBoard() {
    try {
        await navigator.clipboard.writeText(code);
    } catch(err) {

    }
}
</script>

<div class="page bg-dark">
    <section>
        <h1>"Installation"</h1>
        <h2>... if you can call it that</h2>
    </section>
    
    <section>
        <p>Copy this code into a <code>.css</code> file to get started!</p>
    
    </section>
    <div class="code">
        <div class="wide-button">
            <p class="text-highlight">Code</p>
            <button class="btn-hollow text-sm" on:click={copyToClipBoard}>Copy</button>
        </div>
        <code>
            {code}
        </code>
    </div>

    <section>
        <p>If you're still here, go to <a href="/docs">Docs</a> to learn more!</p>
    </section>
</div>

<style>
    .page {
        min-height: 100vh;
        min-height: 100dvh;
    }
    .code {
        width: 50%;
        margin: auto;
        background-color: var(--background-secondary);
        border-radius: 1em;
        padding: 1em;
    }
    .wide-button {
        width: 100%;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    .wide-button > * {
        margin: 0.5rem;
    }
</style>
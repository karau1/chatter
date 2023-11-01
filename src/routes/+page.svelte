<script>
    import Navigation from "../components/Navigation.svelte";
    import Hamburger from "../components/Hamburger.svelte";

    let isNavVisible = false;

    function handleNavToggle() {
        isNavVisible = !isNavVisible;
    }
</script>

<header>
    <div>
        {#if isNavVisible}
            <Navigation visible={isNavVisible}/>
        {/if}
    </div>
</header>

<main>
    <Hamburger on:toggle={handleNavToggle}/>
    <div class="hero">
        <h1 class="title">Chatter</h1>
    </div>
</main>

<style>
    .hero {
        padding: 0.75rem 0;
        background: #1b368a;
        height: 4rem;
    }

    .title {
        font-family: 'Roboto Mono', monospace;
        text-align: center;
        margin: 0;
        color: white;
    }

    header {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        z-index: 1; /* Ensure the header is below hero content */
    }
</style>
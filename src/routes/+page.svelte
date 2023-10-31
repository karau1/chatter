<script>
    import Navigation from "../components/Navigation.svelte";
    import Hamburger from "../components/Hamburger.svelte";

    let isNavVisible = false;
    function handleNavToggle() {
        isNavVisible = !isNavVisible;
    }
</script>

<main>

    <header>
        <div>
            <Hamburger on:toggle={handleNavToggle} />
            {#if isNavVisible}
                <Navigation visible={isNavVisible}/>
            {/if}
        </div>
    </header>
</main>

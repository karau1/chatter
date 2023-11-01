<script lang="ts">
    import { createEventDispatcher } from 'svelte';

    const dispatch = createEventDispatcher();

    function toggleNav() {
        dispatch('toggle', {});
    }
</script>


<button on:click={toggleNav} class="nav-toggle">
    <span class="hamburger" ></span>
</button>

<style>
    .nav-toggle {
        z-index: 1;
        cursor: pointer;
        border: 0;
        width: 3em;
        height: 3em;
        padding: 0;
        border-radius: 50%;
        background: #9bbbff;
        color: white;
        transition: opacity 250ms ease;
        margin-left: 0.75em;
        margin-top: 0.75rem;

        position: absolute;
    }

    .hamburger {
        width: 50%;
        position: relative;
    }

    .hamburger,
    .hamburger::before,
    .hamburger::after {
        display: block;
        margin: 0 auto;
        height: 3px;
        background: #ffffff;
    }

    .hamburger::before,
    .hamburger::after {
        content: '';
        width: 100%;
    }

    .hamburger::before {
        transform: translateY(-6px);
    }

    .hamburger::after {
        transform: translateY(3px);
    }

</style>

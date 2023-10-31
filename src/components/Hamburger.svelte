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
        cursor: pointer;
        border: 0;
        width: 3em;
        height: 3em;
        padding: 0;
        border-radius: 50%;
        background: #2662e3;
        color: white;
        transition: opacity 250ms ease;

        position: absolute;
        left: 0.75em;
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
        background: #dc2929;
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

<nav class="navigation">
    <ul>
        <li class="nav_list_point"><a class="nav_link" href="/">Home</a></li>
        <li class="nav_list_point"><a class="nav_link" href="/about">About</a></li>
        <li class="nav_list_point"><a class="nav_link" href="/contacts">Contacts</a></li>
    </ul>
</nav>

<style>

    .navigation {
        background-color: #4369c0;
        padding: 1em;
        margin-top: 4rem;
    }

    .navigation ul {
        padding: 0 4em;
    }

    .nav_list_point {
        list-style: none;
    }

    .nav_list_point + .nav_list_point {
        list-style: none;
        margin-top: 1em;
    }

    .nav_link {
        text-decoration: none;
        background: #1b368a;
        border-radius: 4px;
        color: white;
        display: block;
        text-align: center;
        padding: 0.25em;
        border: 2px solid white;
    }

    @media (min-width: 599px) {
        .navigation ul {
            display: flex;
            margin: 0;
            padding: 0;
        }

        .navigation li {
            list-style: none;
            margin-right: 1em;
        }
    }
</style>

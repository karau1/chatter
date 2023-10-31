<nav class="navigation">
    <ul>
        <li><a href="/">Home</a></li>
        <li><a href="/about">About</a></li>
        <li><a href="/contacts">Contacts</a></li>
    </ul>
</nav>

<style>

    .navigation {
        background-color: #b02e2e;
        padding: 1em;
    }

    .navigation ul {
        padding: 0;
        margin: 0;
    }

    .navigation li {
        list-style: none;
        margin-bottom: 1em;
    }
    .navigation a {
        text-decoration: none;
        color: black;
        display: block;
        text-align: center;
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

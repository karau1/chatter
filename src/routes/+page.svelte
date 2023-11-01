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
    <div class="main">
        <div class="row">
            <div class="image chatter_img">
                <img src="/chat_image1.png" alt="chatter">
            </div>
        </div>

    </div>
    <div class="improvements">
        <div class="row ">
            <div class="improvement improvement1">
                <p>We will improve the quality of the services</p>
                <div class="centered_img image">
                    <img src="/Gear-icon.png" alt=""/>
                </div>
            </div>
            <div class="improvement improvement2">
                <p>Make awesome experience with our packets</p>
                <div class="centered_img image">
                    <img src="/experience.png" alt=""/>
                </div>
            </div>
        </div>
        <div class="row ">
            <div class="improvement improvement3">
                <p>Meet yourself with futurstic user expiences</p>
                <div class="centered_img image">
                    <img src="/ux.png" alt=""/>
                </div>
            </div>
            <div class="improvement improvement4">
                <p>Discover new worlds using our pro packet</p>
                <div class="centered_img image">
                    <img src="/star.png" alt=""/>
                </div>
            </div>
        </div>
    </div>

    <div class="offers">
        <div class="offer">
            <p>Offer Standard pack</p>
            <ul>
                <li>Lorem ipsum dolor sit amet</li>
                <li>consectetur adipisicing elit</li>
                <li>Aperiam, asperiores, blanditiis consequatur</li>
                <li>ipsum dolor sit amet</li>
            </ul>
        </div>

        <div class="offer">
            <p>Offer Premium pack</p>
            <ul>
                <li>Lorem ipsum dolor sit amet</li>
                <li>consectetur adipisicing elit</li>
                <li>Aperiam, asperiores, blanditiis consequatur</li>
                <li>ipsum dolor sit amet</li>
            </ul>
        </div>

        <div class="offer">
            <p>Offer Energy pack</p>
            <ul>
                <li>Lorem ipsum dolor sit amet</li>
                <li>consectetur adipisicing elit</li>
                <li>Aperiam, asperiores, blanditiis consequatur</li>
                <li>ipsum dolor sit amet</li>
            </ul>
        </div>

    </div>

    <div class="donations">
<!--        Donate-->
        <p>Donate!</p>
    </div>

    <footer>

    </footer>
</main>

<style>
    * {
        font-family: 'Roboto Mono', monospace;
    }

    ul {
        list-style: none;
        margin-left: 0;
        padding-left: 0;
    }

    li {
        padding-left: 1em;
        text-indent: -1em;
    }

    li:before {
        content: "+";
        padding-right: 5px;
    }

    .donations {
        height: 10vh;
        background-image: linear-gradient(160deg, #5acec2 0%, #fcc84a 100%);
        margin: 2em auto;
        border-radius: .5rem;
        width: 60%;
        text-align: center;
        vertical-align: middle;
        align-items:center;
        justify-content:center;
        display:flex;
    }

    .donations p {
        font-size: 2.25rem;
        font-weight: bolder;
        color: #083454;
    }

    .offer {
        padding: 10px;
        height: 22vh;
        background-image: linear-gradient(160deg, #d9d1bb 0%, #7370b9 100%);
        margin: 2em 0.5rem 0 0.5rem;
        border-radius: 0.5rem;
    }

    .offer p {
        font-size: 1.25rem;
        font-weight: bolder;
        color: #083454;
    }

    main {
        background-color: #0095d2;
        background-image: linear-gradient(0deg, #0095d2 0%, #303fa5 33%, #4452dc 66%, #5278ff 100%);
    }

    .image {
        margin: 0;
        padding: 0;
    }

    .image img {
        width: 100%; /* Make the image fill the container width */
        height: auto; /* Maintain the aspect ratio of the image */
    }

    .chatter_img {
        z-index: 1;
    }

    .centered_img {
        margin: 0 auto;
        width: 50px;
        height: 100px;
    }

    p {
        font-family: 'Roboto Mono', monospace;
    }

    .improvement {
        width: 50%;
        height: 10rem;
        background-image: linear-gradient(160deg, #2a5f85 0%, #7370b9 100%);
        margin: 0.5rem;
        text-align: center;
        padding: 10px;
        border-radius: 0.5rem;
        color: white;
    }

    .improvement2 {
        background-image: linear-gradient(160deg, #083454 0%, #7878b4 100%);
    }

    .improvement3 {
        background-image: linear-gradient(160deg, #5151c7 0%, #7878b4 100%);
    }

    .improvement4 {
        background-image: linear-gradient(160deg, #1b689a 0%, #7878b4 100%);
    }

    .main {
        height: 40vh;
    }

    .row {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
    }

    .hero {
        padding: 0.75rem 0;
        background-color: #08AEEA;
        background-image: linear-gradient(0deg, #08AEEA 0%, #2135d3 100%);
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
        z-index: 2; /* Ensure the header is below hero content */
    }
</style>

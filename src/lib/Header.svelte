<svelte:head>
  <link rel="stylesheet" href="css/main.css" />
</svelte:head>

<header>
    <h1>
    Dracula.net
    </h1>
    <div class="buttoncontain">
        <nav>
            <a href="/">
                <button>Home</button>
            </a>
            <a href="about">
                <button>About</button>
            </a>
            <a href="gallery">
                <button>Gallery</button>
            </a>
            <a href="contact">
                <button>Contacts</button>
            </a>
        </nav>

    </div>
</header>
<style>

button{
    background-color: #222222;
    color: #8f9596;
    font-weight: bold;
    font-size: larger;
    font-family: sans-serif;
    padding-left: 10px;
    padding-bottom: 5px;
    border: #8f9596;
}

button:hover{
    color:#dcd9dd;

}

h1 {
    margin: 0px;
    background-color: #222222;
    color: #dcd9dd;
    font-family: sans-serif;
    padding-top: 10px;
    padding-left: 10px;
}
nav {
    background-color: #222222;
}

header {
    position: sticky;
    top: 0;
}

</style>
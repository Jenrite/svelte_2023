<script>
    
</script>
<header>
        <a class="logo" href= "/">VAMPIRE.NET</a>
        <nav>
            <ul class="nav__links">
                <li><a href="/about">About</a></li>
                <li><a href="/contact">Gallery</a></li>
                <li><a href="/cards">Cards
                </a></li>
            </ul>
        </nav>
        <a class="cta" href="/contact"><button>Contact</button></a>
</header>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto+Mono&display=swap');

li, a, button {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
    font-weight: 500;
    font-size: 16px;
    color: #edf0f1;
    text-decoration: none;
}

.logo {
    font-family: 'Roboto Mono', monospace;
    font-size: 25px;
    color: #edf0f1;
    text-decoration: none;
    margin-left: 10px;
    
}

header {

    margin: 10px;
    display:flex;
    justify-content: space-between;
    align-items: center;
    background-color: #2d333a;
    border: none;
    border-radius: 10px;
}
.logo {
    cursor: pointer;
}
.nav__links {
    list-style: none;
}

.nav__links li {
    display: inline-block;
    padding: 0px 20px;
}

.nav__links li a {
    transition: all 0.3s ease 0s;
}

.nav__links li a:hover {
    color: rgba(229, 75, 75 ,1)
}

button {
    padding: 9px 25px;
    background-color: rgba(229, 75, 75 ,1);
    border: none;
    border-radius: 10px;
    cursor: pointer;
    transition: all 0.3s ease 0s;
    margin-right: 10px;

}

button:hover {
    background-color: rgba(229, 75, 75 ,0.8);
}

</style>
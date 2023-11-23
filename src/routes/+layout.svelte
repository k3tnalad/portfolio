
<script>
    import '../app.css'
    export let theme;


    function toggleTheme(){
        if(typeof window !== 'undefined' && typeof localStorage !== 'undefined'){
        localStorage.setItem('theme', theme? 'light' : 'dark') 
        theme = !theme;
        }
    }
</script>

<main class:light={!theme} class:dark={theme}>
    <slot></slot>
    <section class="navigation">
            <section class="links">
                <a href="/">HOME</a>
                <a href="/works">WORKS</a>
                <a href="https://hecking-blog.netlify.app">BLOG</a>
                <a href="/contacts">CONTACTS</a>
            </section>
        <button class:light={!theme} class:dark={theme} on:click={toggleTheme}>{theme? "LIGHT MODE" : "DARK MODE"}</button>
    </section>
</main>

<style>
    main {
        height: 100vh;
        display: grid;
        grid-template-rows: 82% 18%;
        padding: 3em;
    }
    main.light {
        background: rgb(175, 184, 190);
        background: linear-gradient(100deg, rgb(215, 221, 224) 0%, hsla(191, 5%, 40%, 1) 100%);
        background: -moz-linear-gradient(100deg, rgb(215, 221, 224) 0%, hsla(191, 5%, 40%, 1) 100%);
        background: -webkit-linear-gradient(100deg, rgb(215, 221, 224) 0%, hsla(191, 5%, 40%, 1) 100%);
        color: black;
    }
    main.dark {
        background: #191a1b;
        background: linear-gradient(100deg, rgb(46, 46, 46) 0%, hsla(191, 5%, 40%, 1) 100%);
        background: -moz-linear-gradient(100deg, rgb(46, 46, 46) 0%, hsla(191, 5%, 40%, 1) 100%);
        background: -webkit-linear-gradient(100deg, rgb(46, 46, 46) 0%, hsla(191, 5%, 40%, 1) 100%);
        color: white;
    }
    section.navigation {
        display: flex;
        align-items: end;
        justify-content: space-between;
        width: 100%;
    }
    section.links {
        display: flex;
        gap: 1em;
    }
    section.links > a {
        font-size: 32px;
        color: inherit;
        transition: all 150ms ease-out;
    }
    section.links > a:hover {
        color: #7c7f81;
    }
    button.light {
        border: none;
        background: none;
        cursor: pointer;
        font-size: 18px;
        color: inherit;
    }
    button.dark {
        border: none;
        background: none;
        cursor: pointer;
        font-size: 18px;
        color: whitesmoke;
    }
  </style>
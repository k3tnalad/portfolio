<script>
    import {fly} from 'svelte/transition';
</script>

<section class="main">
    <section>
        <h1>KYRYLO BATKOVICH</h1>
        <p>I'M KYRYLO, A WEB DEV, WHO LIKES COFFEE, POPSCI BOOKS, AND RUNNING</p>
    </section>
    <div class="comp">
        <img in:fly={{duration: 300, y: 470, x: -150}} src="src/lib/assets/image17.png" alt="computer" srcset="">
    </div>
</section>

<style>
    div.comp {
        display: grid;
        place-items: center;
    }
 img {
    padding-top: 3em;
    width: 1000px;
 }

</style>
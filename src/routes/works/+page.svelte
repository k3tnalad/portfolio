<script>
    import '../../app.css'
</script>

<main>
    <div class="container">
        <div class="cards">
            <div class="card first">
                <h4>Test title</h4>
                <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Porro temporibus consequatur tempore nemo impedit mollitia.</p>
            </div>
            <div class="card">
                <h4>Test title</h4>
                <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Porro temporibus consequatur tempore nemo impedit mollitia.</p>
            </div>
            <div class="card">
                <h4>Test title</h4>
                <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Porro temporibus consequatur tempore nemo impedit mollitia.</p>
            </div>
        </div>
    </div>
</main>

<style>
    main {
        border: 1px solid grey;
    }
    div.container {
        height: 100%;
    }
    div.cards {
        height: 100%;
        width: 100%;
        display: grid;
        grid-template-columns: repeat(3, 1fr);
    }
    div.card {
        width: auto;
        padding: 2em;
        border: 1px solid black;
        color: white;
    }
    div.first {
        background: hsla(101, 85%, 16%, 0.5);
    }
</style>
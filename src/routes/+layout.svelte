<script>import "../app.pcss";</script>
<slot></slot>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Open+Sans:ital,wght@0,300..800;1,300..800&display=swap');
    :global(body) {
        color: white;
        background-image: linear-gradient(#627BFF -600%, #080A0B);
        background-repeat: no-repeat;
        background-size: cover;
        background-attachment: fixed;
        font-family: 'Bebas Neue', sans-serif;
    }

    :global(button) {
        font-family: 'Open Sans', sans-serif;
    }
</style>

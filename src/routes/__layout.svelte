<script lang="ts">
	import '../app.css';
    import '../timeline.css';
</script>

<div class="primary app-container">
    <div class="app-header desktop">Kyrstin Lou Ward and Edwin Michael Ward III</div>
    <div class="app-header mobile">Lou and Teddy</div>
    <nav>
        <a href="/">Home</a>
        <a href="/schedule">Schedule</a>
        <a href="/rsvp">RSVP</a>
        <a href="/durham">Durham</a>
        <a href="/photos">Photos</a>
        <a href="/faq">FAQ</a>
    </nav>
    <div class="page-slot">
        <slot></slot>
    </div>
</div>

<style>
	.app-container {
        display: flex;
        flex-direction: column;
        font-family: 'Montserrat', sans-serif;
        height: 100%;
		width: 100%;
	}
    .app-header {
        font-family: 'Bodoni Moda', serif;
        font-size: 36px;
        line-height: 4rem;
        margin-top: 2%;
        min-height: 4rem;
        text-align: center;
        width: 100%;
    }
    nav {
        align-items: center;
        display: flex;
        justify-content: space-evenly;
        line-height: 3rem;
        min-height: 3rem;
        width: 100%;
    }
    nav a {
        color: inherit;
        text-decoration: none;
        flex-grow: 1;
        text-align: center;
    }
    .page-slot {
        align-items: center;
        display: flex;
        flex-direction: column;
        height: 100%;
        overflow: scroll;
        width: 100%;
    }
    :global(.page-header-image) {
        display: block;
        max-width: 95%;
        min-width: 85%;
        max-height: 80%;
        height: auto;
    }
    :global(.page-title) {
        display: flex;
        flex-direction: row;
        font-size: 24px;
        justify-content: space-around;
        margin-top: 20px;
        width: 100%;
    }
    :global(.page-content) {
        line-height: 28px;
        margin-top: 25px;
        text-align: center;
        width: 65%;
    }

    @media only screen and (min-width: 800px) {
        :global(.desktop) {
            display: initial;
        }
        :global(.mobile) {
            display: none;
        }
    }
    @media only screen and (max-width: 799px) {
        :global(.desktop) {
            display: none;
        }
        :global(.mobile) {
            display: initial;
        }
    }
</style>

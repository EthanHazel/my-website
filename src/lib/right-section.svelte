<script>
</script>

<div id="right-section" class="section">
    <picture class="portrait">
        <source media="(min-width:1080px)" srcset="./portrait/1080.webp" />
        <source media="(min-width:1024px)" srcset="./portrait/1024.webp" />
        <source media="(min-width:720px)" srcset="./portrait/720.webp" />
        <source media="(min-width:512px)" srcset="./portrait/512.webp" />
        <source media="(min-width:480px)" srcset="./portrait/480.webp" />
        <source media="(min-width:360px)" srcset="./portrait/360.webp" />
        <img src="./portrait/2048.webp" alt="portrait" class="portrait" />
    </picture>

    <div id="background"></div>
</div>

<style>
    @keyframes spin {
        from {
            transform: translate(-50%, -50%) rotate(0deg);
        }
        to {
            transform: translate(-50%, -50%) rotate(360deg);
        }
    }

    @keyframes fade-in {
        0% {
            opacity: 0;
        }
        50% {
            opacity: 0;
        }
        100% {
            opacity: 1;
        }
    }

    #right-section {
        position: relative;
        overflow: hidden;
        mix-blend-mode: lighten;
        animation: fade-in 1s ease-in-out;
    }

    .portrait {
        height: 100%;
        width: 100%;
        object-fit: cover;
        object-position: left bottom;
        z-index: 2;
    }

    #background {
        position: absolute;
        top: 50%;
        left: 50%;
        display: block;
        width: 100vh;
        height: 100vh;
        background-image: url(./portrait/spiral.svg);
        background-size: cover;
        background-position: center;
        transform: translate(-50%, -50%);
        animation: spin 10s linear infinite;
        z-index: 1;
    }
</style>

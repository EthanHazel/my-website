<script>
    import Links from "./links.svelte";
    import Logo from "./icons/logo.svelte";

    import LINKS from "../data/links.json";
</script>

<div id="left-section" class="section">
    <h1 id="logo">
        <Logo size={48} /> Ethan Hazel
    </h1>
    <p>
        <span class="selected">I'm a Graphic Designer &amp; Web Developer</span
        >{" "}
        focused on creating open source projects with great user experience. Currently
        building things over at{" "}
        <a href={LINKS.phosphorus} target="_blank" rel="noopener noreferrer"
            >Phosphorus</a
        >.
    </p>
    <p>
        I design and build with the user in mind first, always. Good experiences
        earn trust, and trust is worth a whole lot more than a quick win.
    </p>
    <p>Reach out on any of the channels below if you have any inquiries.</p>

    <Links />
</div>

<style>
    #left-section {
        justify-content: space-between;
        align-items: flex-start;
        padding: 3rem;
    }

    h1 {
        margin: 0;
        letter-spacing: -1px;
    }

    a {
        color: var(--text-color);
    }

    #logo {
        display: flex;
        align-items: center;
        gap: 2rem;
    }

    @media (max-width: 800px) {
        :global(#logo svg) {
            width: 36px;
            height: 36px;
        }

        #logo {
            gap: 1rem;
        }

        #left-section {
            padding: 1rem;
        }
    }
</style>

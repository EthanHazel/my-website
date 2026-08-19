<script>
    import LINKS from "../data/links.json";

    import { SiGithub, SiX } from "@icons-pack/svelte-simple-icons";
    import { Mail } from "@lucide/svelte";
    import Linkedin from "./icons/linkedin.svelte";
    import Phosphorus from "./icons/phosphorus.svelte";
</script>

<div id="links">
    <a class="link" href={LINKS.email} target="_blank">
        <Mail />
    </a>

    <a class="link" href={LINKS.github} target="_blank">
        <SiGithub />
    </a>

    <a class="link" href={LINKS.twitter} target="_blank">
        <SiX />
    </a>

    <a class="link" href={LINKS.linkedin} target="_blank">
        <Linkedin />
    </a>

    <a class="link" href={LINKS.phosphorus} target="_blank">
        <Phosphorus />
    </a>
</div>

<style>
    #links {
        display: flex;
        flex-direction: row;
        gap: 1rem;
    }

    .link {
        display: flex;
        align-items: center;
        justify-content: center;
        width: 2rem;
        height: 2rem;
        color: var(--text-color);

        &:hover {
            opacity: 50%;
        }

        &:active {
            opacity: 25%;
        }
    }
</style>

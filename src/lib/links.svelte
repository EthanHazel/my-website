<script>
    import LINKS from "../data/links.json";

    import { SiGithub, SiX } from "@icons-pack/svelte-simple-icons";
    import { Mail } from "@lucide/svelte";
    import Linkedin from "./icons/linkedin.svelte";
    import Phosphorus from "./icons/phosphorus.svelte";
</script>

<div id="links">
    <a class="link" href={LINKS.email} target="_blank">
        <Mail size={16} />
    </a>

    <a class="link" href={LINKS.github} target="_blank">
        <SiGithub size={16} />
    </a>

    <a class="link" href={LINKS.twitter} target="_blank">
        <SiX size={16} />
    </a>

    <a class="link" href={LINKS.linkedin} target="_blank">
        <Linkedin size={16} />
    </a>

    <a class="link" href={LINKS.phosphorus} target="_blank">
        <Phosphorus size={16} />
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
        width: 1.5rem;
        height: 1.5rem;
        color: var(--text-color);

        @media (hover: hover) {
            &:hover {
                opacity: 50%;
            }
        }

        &:active {
            opacity: 25%;
        }
    }
</style>

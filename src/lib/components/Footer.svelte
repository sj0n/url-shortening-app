<script>
    import FooterBrandWrapper from "./FooterBrandWrapper.svelte";
    import FooterLinksWrapper from "./FooterLinksWrapper.svelte";
    import FooterSocialsWrapper from "./FooterSocialsWrapper.svelte";
</script>
<section>
    <div class="wrapper">
        <FooterBrandWrapper />
        <FooterLinksWrapper />
        <FooterSocialsWrapper />
    </div>
</section>
<style>
    section {
        background-color: var(--neutral-darkviolet);
    }

    .wrapper {
        display: flex;
        justify-content: space-between;
        max-width: 1170px;
        margin-left: auto;
        margin-right: auto;
    }

    @media (min-width: 60rem) {
        section {
            padding: 4rem 2rem;
        }
    }

    @media screen and (max-width: 60rem) {
        section {
            padding: 2rem;
        }

        .wrapper {
            flex-direction: column;
        }
    }
</style>
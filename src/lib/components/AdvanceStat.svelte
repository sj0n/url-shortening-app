<script>
    import FormWrapper from "./FormWrapper.svelte";
    import StatHeadingWrapper from "./StatHeadingWrapper.svelte";
    import FeatureWrapper from "./FeatureWrapper.svelte";
</script>

<section>
    <div class="wrapper">
        <FormWrapper />
        <StatHeadingWrapper />
        <FeatureWrapper />
    </div>
</section>
<style>
    section {
        background-color: hsl(225, 33.3%, 95.3%);
    }

    .wrapper {
        max-width: 1170px;
        margin-left: auto;
        margin-right: auto;
        padding: 2rem 1rem 10rem 1rem;
    }
</style>
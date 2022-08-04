<section>
    <div class="wrapper">
        <h1>Boost your links today</h1>
        <a href="#getstarted" class="btn-primary">Get Started</a>
    </div>
</section>
<style>
    section {
        background-color: var(--primary-darkviolet);
        background-repeat: no-repeat;
        background-size: cover;
        background-position: center;
        color: var(--neutral-white);
        text-align: center;
    }

    .wrapper {
        max-width: 1170px;
        margin-left: auto;
        margin-right: auto;
    }

    .wrapper h1 {
        font-size: 2.2rem;
        margin-bottom: 1.5rem;
    }

    .btn-primary {
        background-color: var(--primary-cyan);
        border-radius: 20px;
        color: var(--neutral-white);
        font-weight: 700;
        padding: 0.6rem 2rem;
        text-decoration: none;
        user-select: none;
    }

    .btn-primary:hover {
        background-color: var(--primary-lightcyan);
    }

    @media (min-width: 60rem) {
        section {
            background-image: url("/images/bg-boost-desktop.svg");
            padding: 3rem;
        }
    }

    @media screen and (max-width: 60rem) {
        section {
            background-image: url("/images/bg-boost-mobile.svg");
            padding: 4rem 1.2rem;
        }
        .wrapper h1 {
            font-size: 1.5rem;
        }
    }
</style>
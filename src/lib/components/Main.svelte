<main>
    <section>
            <h1>More than just shorter links.</h1>
            <p>
                Build your brand's recognition and get detailed insights on how
                your links are performing.
            </p>
            <a href="#getstarted" class="btn-primary">Get Started</a>
    </section>
</main>

<style>
    main {
        background-image: url('/images/illustration-working.svg');
        background-repeat: no-repeat;
    }

    section {
        max-width: 1170px;
        margin-left: auto;
        margin-right: auto;
        padding: 5rem 1rem 15rem 1rem;
    }

    h1 {
        color: var(--neutral-darkblue);
        max-width: 550px;
        font-size: clamp(2.5rem, 6vw, 4rem);
        line-height: 1.2;
    }

    p {
        color: var(--neutral-grayishviolet);
        max-width: 450px;
        margin-top: 1rem;
    }

    .btn-primary {
        background-color: var(--primary-cyan);
        border-radius: 40px;
        padding: 0.5rem 1.5rem;
        margin-top: 1.5rem;
        display: inline-block;
        color: var(--neutral-white);
        text-decoration: none;
        font-weight: 700;
    }

    .btn-primary:hover {
        background-color: var(--primary-lightcyan);
    }

    @media (min-width: 60rem) {
        main {
            background-position: 750px 10px;
        }
    }

    @media screen and (max-width: 60rem) {
        main {
            background-position: 50px top;
            background-size: contain;
        }

        section {
            text-align: center;
            padding: 16rem 1rem 10rem 1rem;
        }
    }
</style>

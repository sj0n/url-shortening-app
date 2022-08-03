<div class="features-flex">
    <div class="feature-card">
        <span>
            <img
                src="/images/icon-brand-recognition.svg"
                alt="Ascending graph icon"
            />
        </span>
        <h2>Brand Recognition</h2>
        <p>
            Boost your brand recognitionw with each click. Generic links
            don't mean a thing. Branded inks help instill confidence in
            your content.
        </p>
    </div>
    <div class="feature-card">
        <span>
            <img
                src="/images/icon-detailed-records.svg"
                alt="Meter icon"
            />
        </span>
        <h2>Detailed Records</h2>
        <p>
            Gain insights nto who is clicking your links. Knowing when
            and where people engage with your content helps inform
            better decisions.
        </p>
    </div>
    <div class="feature-card">
        <span>
            <img
                src="/images/icon-fully-customizable.svg"
                alt="Paint brush icon"
            />
        </span>
        <h2>Fully Customizable</h2>
        <p>
            Improve brand awareness and conent discoverability thorugh
            customizable links, supercharging audience engagement.
        </p>
    </div>
</div>
<style>
    .features-flex {
        display: flex;
        font-size: 16px;
        gap: 2rem;
        margin-top: 5rem;
        position: relative;
    }

    .feature-card {
        background-color: hsl(255, 100%, 100%);
        border-radius: 5px;
        max-width: 400px;
        min-width: 350px;
        padding: 3.5rem 2rem 2rem 2rem;
        position: relative;
        z-index: 2;
    }

    .feature-card span {
        background-color: var(--primary-darkviolet);
        border-radius: 50%;
        padding: 1rem;
        position: absolute;
    }

    .feature-card h2 {
        color: var(--neutral-darkblue);
        font-size: 1.2rem;
        margin-bottom: 0.8rem;
    }

    .feature-card p {
        color: var(--neutral-grayishviolet);
    }

    .feature-card:nth-child(2) {
        transform: translateY(40px);
    }

    .feature-card:nth-child(3) {
        transform: translateY(80px);
    }

    @media (min-width: 60rem) {
        .features-flex:not(:first-child)::before {
            content: " ";
            width: 70%;
            height: 10px;
            background-color: var(--primary-cyan);
            position: absolute;
            z-index: 1;
            top: 130px;
        }

        .feature-card span {
            top: -40px;
        }
    }

    @media screen and (max-width: 60rem) {
        .features-flex {
            flex-direction: column;
            text-align: center;
        }

        .features-flex:not(:first-child)::before {
            content: " ";
            width: 10px;
            height: 98%;
            background-color: var(--primary-cyan);
            position: absolute;
            z-index: 1;
            left: 183px;
        }

        .feature-card span {
            top: -40px;
            left: 150px;
        }
    }
</style>
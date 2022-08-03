<script>
let error = false;
    let url = "";
    let urls = localStorage.getItem("urls")
        ? JSON.parse(localStorage.getItem("urls"))
        : [];
    const shortenLink = async (e) => {
        e.preventDefault();
        if (!url) {
            error = true;
        }
        if (url) {
            if (!localStorage.getItem('urls')) {
                const shorten = await (await fetch(`https://api.shrtco.de/v2/shorten?url=${url}`)).json();
                urls = [{url, shorten}];
                localStorage.setItem('urls', JSON.stringify(urls));
            } else {
                const shorten = await (await fetch(`https://api.shrtco.de/v2/shorten?url=${url}`)).json();
                urls = JSON.parse(localStorage.getItem('urls'));
                if (urls.length === 3) urls.shift();
                urls = [...urls, {url, shorten}];
                localStorage.setItem('urls', JSON.stringify(urls));
            }
            url = "";
            error = false;
        }
    };
    let copyLink = async (e) => {
        await navigator.clipboard.writeText(
            e.target.previousElementSibling.href
        );
        e.target.textContent = "Copied!";
        e.target.style.backgroundColor = `var(--primary-darkviolet)`;
    };
</script>
<div class="form-offset">
    <form class="form-wrapper" on:submit={shortenLink}>
        <div class="form-control">
            <input
                type="text"
                name="link"
                id="link"
                placeholder="Shorten a link here..."
                class="input-text"
                class:error
                bind:value={url}
            />
            <p id="alert" class:error>Please enter a valid address.</p>
        </div>
        <input type="submit" value="Shorten It!" class="input-submit" />
    </form>

    {#each urls as url, index (index)}
        <div class="shorten-link-wrapper">
            <div class="plain-url">{url.url}</div>
            <div class="shorten-link-aside">
                <a href={url.shorten.result.full_short_link} target="_blank" rel="noopener">{url.shorten.result.full_short_link}</a>
                <button class="btn-primary" on:click={copyLink}
                    >Copy</button
                >
            </div>
        </div>
    {/each}
</div>
<style>
    .form-offset {
        transform: translateY(-100px);
    }

    .form-wrapper {
        background-color: var(--primary-darkviolet);
        background-repeat: no-repeat;
        border-radius: 10px;
        display: flex;
        gap: 20px;
        margin-bottom: 1rem;
    }

    .form-control {
        width: 100%;
        position: relative;
    }

    .form-control p {
        display: none;
        position: absolute;
    }

    .form-control p.error {
        display: block;
        color: hsl(0, 45%, 60%);
    }

    .input-text {
        border-radius: 10px;
        padding: 0.5rem 1rem;
        width: 100%;
    }

    .input-text.error {
        border-color: hsl(0, 45%, 60%);
    }

    .input-submit {
        background-color: var(--primary-cyan);
        border-radius: 10px;
        border-width: 0;
        color: var(--neutral-white);
        cursor: pointer;
        padding: 0.5rem 2rem;
        font-weight: 700;
    }

    .input-submit:hover {
        background-color: var(--primary-lightcyan);
    }

    .shorten-link-wrapper {
        background-color: hsl(0, 0%, 100%);
        border-radius: 5px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .shorten-link-wrapper:not(:last-child) {
        margin-bottom: 1rem;
    }

    .plain-url {
        color: var(--primary-darkviolet);
        text-overflow: ellipsis;
        overflow: hidden;
    }

    .shorten-link-aside a {
        color: var(--primary-cyan);
        margin-right: 1rem;
        text-decoration: none;
        text-overflow: ellipsis;
    }

    .btn-primary {
        background-color: var(--primary-cyan);
        border-width: 0;
        border-radius: 7px;
        color: var(--neutral-white);
        cursor: pointer;
        font-weight: 700;
        padding: 0.5rem 1.5rem;
    }

    .shorten-link-aside button:hover {
        background-color: var(--primary-lightcyan);
    }
    
    @media (min-width: 60rem) {
        .form-wrapper {
            background-image: url("/images/bg-shorten-desktop.svg");
            padding: 2.5rem;
        }

        .shorten-link-wrapper {
            padding: 1rem;
        }
    }

    @media screen and (max-width: 60rem) {
        .form-wrapper {
            background-image: url("/images/bg-shorten-mobile.svg");
            flex-direction: column;
            padding: 1.5rem;
        }

        .shorten-link-wrapper {
            flex-direction: column;
            justify-content: normal;
        }

        .plain-url {
            width: 100%;
            border-bottom: 1px solid var(--neutral-gray);
            padding: 0.8rem;
            max-width: 370px;
        }

        .shorten-link-aside {
            width: 100%;
            padding: 0.8rem;
        }

        .shorten-link-aside > * {
            display: block;
            width: 100%;
        }

        .shorten-link-aside a {
            margin-bottom: 0.8rem;
        }
    }
</style>
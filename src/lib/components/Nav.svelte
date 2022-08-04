<script>
    let active = false;
    const showMenu = (e) => {
        e.stopPropagation();
        const menuList = document.getElementsByClassName("menu-list");
        active = !active;
        menuList[0].classList.toggle("active");
    };
</script>

<nav>
    <div class="lg-only">
        <a href="#home">
            <img src="/images/logo.svg" alt="Shortly Logo" />
        </a>
        <ul>
            <li>
                <a href="#features">Features</a>
            </li>
            <li>
                <a href="#pricing">Pricing</a>
            </li>
            <li>
                <a href="#resources">Resources</a>
            </li>
        </ul>
    </div>
    <ul class="lg-only">
        <li>
            <a href="#login">Login</a>
        </li>
        <li class="btn-primary">
            <a href="#signup">Sign Up</a>
        </li>
    </ul>
    <a href="#home"><img src="/images/logo.svg" alt="Shortly Logo" /></a>
    <div class="menu-wrapper">
        <button on:click={showMenu} id="menu" class="menu-btn" role="menu">
            <img src="/images/menu.svg" alt="Menu Icon" />
        </button>
        <ul class="menu-list" class:active>
            <li>
                <a href="#features">Features</a>
            </li>
            <li>
                <a href="#pricing">Pricing</a>
            </li>
            <li>
                <a href="#resources">Resources</a>
            </li>
            <hr />
            <li>
                <a href="#login">Login</a>
            </li>
            <li class="btn-primary">
                <a href="#signup">Sign Up</a>
            </li>
        </ul>
    </div>
</nav>

<style>
    nav {
        display: flex;
        max-width: 1170px;
        margin-left: auto;
        margin-right: auto;
        padding: 2rem 1rem;
        justify-content: space-between;
        user-select: none;
    }

    nav > div {
        display: flex;
    }

    nav ul li {
        display: inline;
    }

    li:not(:last-child) {
        margin-right: 1rem;
    }

    li a {
        text-decoration: none;
        color: var(--neutral-grayishviolet);
        font-weight: 700;
        font-size: 16px;
    }

    li a:hover {
        color: var(--neutral-darkblue);
    }

    .btn-primary {
        background-color: var(--primary-cyan);
        border-radius: 40px;
        color: hsl(0, 0%, 95%);
        padding: .5rem;
    }

    .btn-primary a {
        color: hsl(0, 0%, 95%);
        padding: .5rem 1.5rem;
    }

    .btn-primary:hover {
        background-color: hsl(180, 66%, 70%);
    }

    .btn-primary:hover a {
        color: hsl(0, 0%, 95%);
    }
    
    @media screen and (max-width: 60rem) {
        .lg-only {
            display: none;
        }

        .menu-btn {
            width: 2rem;
            height: 2rem;
            background-color: transparent;
            border-style: none;
            cursor: pointer;
            padding: 0;
        }

        .menu-btn:active {
            border-style: dotted;
            border-color: black;
        }

        .menu-btn img {
            vertical-align: middle;
        }

        .menu-wrapper {
            position: relative;
            display: inline-block;
        }

        .menu-list {
            position: absolute;
            display: none;
            width: 80vw;
            height: 340px;
            padding: 1rem 1rem;
            text-align: center;
            background-color: var(--primary-darkviolet);
            border-radius: 10px;
            z-index: 1;
            right: 2px;
            top: 50px;
        }

        .menu-list li {
            display: block;
            margin: 0;
            margin-top: 1rem;
        }

        .menu-list li a {
            color: hsl(0, 0%, 95%);
            font-size: 1.05rem;
        }

        .menu-list hr {
            margin-top: 1rem;
            color: var(--neutral-gray);
            background-color: var(--neutral-gray);
            border: none;
            height: 1px;
        }

        .menu-list.active {
            display: block;
        }
    }

    @media (min-width: 60rem) {
        nav > a,
        .menu-wrapper {
            display: none;
        }
    }
</style>

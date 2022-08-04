<div class="footer-links-wrapper">
    <div class="footer-list">
        <h2>Features</h2>
        <ul>
            <li><a href="#linkshortening">Link Shortening</a></li>
            <li><a href="#brandedlinks">Branded Links</a></li>
            <li><a href="#analytics">Analytics</a></li>
        </ul>
    </div>
    <div class="footer-list">
        <h2>Resources</h2>
        <ul>
            <li><a href="#blog">Blog</a></li>
            <li><a href="#developers">Developers</a></li>
            <li><a href="#support">Support</a></li>
        </ul>
    </div>
    <div class="footer-list">
        <h2>Company</h2>
        <ul>
            <li><a href="#about">About</a></li>
            <li><a href="#ourteam">Our Team</a></li>
            <li><a href="#carrers">Careers</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </div>
</div>
<style>
    .footer-links-wrapper {
        display: flex;
        gap: 4rem;
    }

    .footer-list h2 {
        color: var(--neutral-white);
        font-size: 0.8rem;
        margin-bottom: 1rem;
    }

    .footer-list ul {
        font-size: 0.8rem;
        list-style: none;
        padding: 0;
        user-select: none;
    }

    .footer-list ul li:not(:first-child) {
        padding-top: 0.4rem;
    }

    .footer-list a {
        text-decoration: none;
        color: var(--neutral-grayishviolet);
    }

    .footer-list a:hover {
        color: hsl(180, 46%, 54%);
    }

    @media screen and (max-width: 60rem) {
        .footer-links-wrapper {
            flex-direction: column;
            gap: 2rem;
            margin-top: 2rem;
            text-align: center;
        }
    }
</style>
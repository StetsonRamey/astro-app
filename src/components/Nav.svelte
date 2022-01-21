<nav>
    <a class="logolink" href="/">
        <div class="monogram">SR</div>
    </a>
    <a class="link" href="/projects">Portfolio</a>
    <a class="link" href="/about">About</a>
    <a class="social" href="https://github.com/stetsonramey">
        <svg class="socialicon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16">
            <path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.012 8.012 0 0 0 16 8c0-4.42-3.58-8-8-8z" />
          </svg>
    </a>
    <a class="social" href="https://www.linkedin.com/in/stetson-ramey/">
        <svg class="socialicon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path fill-rule="evenodd" clip-rule="evenodd" d="M1 2.838A1.838 1.838 0 0 1 2.838 1H21.16A1.837 1.837 0 0 1 23 2.838V21.16A1.838 1.838 0 0 1 21.161 23H2.838A1.838 1.838 0 0 1 1 21.161V2.838zm8.708 6.55h2.979v1.496c.43-.86 1.53-1.634 3.183-1.634c3.169 0 3.92 1.713 3.92 4.856v5.822h-3.207v-5.106c0-1.79-.43-2.8-1.522-2.8c-1.515 0-2.145 1.089-2.145 2.8v5.106H9.708V9.388zm-5.5 10.403h3.208V9.25H4.208v10.54zM7.875 5.812a2.063 2.063 0 1 1-4.125 0a2.063 2.063 0 0 1 4.125 0z" /></svg>
    </a>
</nav>

<style>
    nav {
        display: flex;
        align-items: center;
        padding: 1rem 2rem;
    }
    .logolink {
        display: block;
        color: var(--t-fg);
        text-decoration: none;
    }
    .link {
        color: var(--t-subdue);
        display: block;
        margin-left: 1rem;
        text-decoration: none;
        font-size: var(--f-d1);
        text-transform: uppercase;
        padding-top: 0.75em;
        padding-bottom: 0.75em;
    }
    .link:focus,
    .link:hover {
        color: var(--t-active);
    }
    .monogram {
        display: flex;
        align-items: center;
        justify-content: center;
        width: 2em;
        height: 2em;
        margin-right: 0.5rem;
        color: var(--c-black);
        font-weight: 900;
        letter-spacing: -0.125rem;
        border: 3px solid currentColor;
        border-radius: 50%;
    }
    .social {
        display: block;
        margin-left: auto;
    }
    .social + .social {
        margin-left: 0.75rem;
    }
    .socialicon {
        display: block;
        width: 1.25rem;
        height: 1.25rem;
        fill: var(--t-subdue);
        transition: fill linear 150ms;
    }
    .socialicon:hover {
        fill: var(--t-active);
    }
</style>

<script>
    import { onMount, onDestroy } from 'svelte';

    let lastScrollY = 0;
    let isHidden = false;

    // Détection du scroll et gestion du header
    const handleScroll = () => {
        const currentScrollY = window.scrollY;

        if (currentScrollY > lastScrollY) {
            isHidden = true;
        } else {
            isHidden = false;
        }

        lastScrollY = currentScrollY;
    };

    onMount(() => {
        window.addEventListener('scroll', handleScroll);

        onDestroy(() => {
            window.removeEventListener('scroll', handleScroll);
        });
    });
</script>

<header class:hide={isHidden}>
    <nav>
        <ul>
            <li><a href="/">Accueil</a></li>
            <li><a href="/projets">Projets</a></li>
            <li><a href="/contact">Contact</a></li>
        </ul>
    </nav>
</header>

<style>
    header {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        background: rgba(0, 0, 0, 0.8);
        color: white;
        padding: 20px;
        transition: transform 0.3s ease;
        z-index: 1000;
    }

    .hide {
        transform: translateY(-100%);
    }

    nav ul {
        list-style: none;
        display: flex;
        gap: 20px;
        justify-content: center;
        margin: 0;
        padding: 0;
    }

    nav a {
        color: white;
        text-decoration: none;
        font-weight: bold;
    }
</style>

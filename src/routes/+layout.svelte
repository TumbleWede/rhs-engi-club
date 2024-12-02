<script lang="ts">
	let { children } = $props();
	import "../app.css";
	import NavButton from "$lib/components/NavButton.svelte";
</script>

<nav id="navbar">
	<div id="header-logo">
		<a href="/"><img id="header-icon" src="/logo.png" alt="Home"/></a>
		<h1 id="header-title">Reedy<br/>Engineering<br/>Club</h1>
	</div>
	<div id="header-nav">
		<NavButton to="/" text="Home" />
		<NavButton to="/about" text="About" />
		<NavButton to="/meetings" text="Meetings" />
		<NavButton to="/shop" text="Shop" />
		<NavButton to="/contact" text="Contact" />
	</div>
</nav>

{@render children()}

<footer>
	<div id="footer-links">
		<a href="/">Home</a>
		<a href="/about">About</a>
		<a href="/meetings">Meetings</a>
		<a href="/shop">Shop</a>
		<a href="/contact">Contact</a>
	</div>
	<p>© 2024 Reedy Engineering Club. All rights reserved.</p>
	<div id="footer-socials">
		<a class="social" href="https://www.instagram.com/reedyengineering/" target="_blank"><img src="/socials/instagram.svg" alt="Instagram"/></a>
		<a id="social-remind" class="social" href="https://www.remind.com/classes/reedytame" target="_blank">
			<img src="/socials/remind.svg" alt="Remind"/>
			<p id="remind-text">@reedytame</p>
		</a>
		<a class="social" href="https://www.tame.org/" target="_blank"><img src="/socials/tame.png" alt="TAME"/></a>
	</div>
	<!---<p>2021 Reedy Engineering Club. All rights reserved.</p>
    <p>Contact us at <a href="mailto:club@reedyengineering.com">club@reedyengineering.com</a></p>
    <p>Website built using <a href="https://svelte.dev/">Svelte</a> and <a href="https://vercel.com/">Vercel</a></p>
    <p>Powered by <a href="https://www.netlify.com/">Netlify</a></p>
    <p>Made with ��️ by the Reedy Engineering Club</p>
    <p>Last updated: {new Date().toLocaleString()}</p>
    <p>Made by <a href="https://github.com/hannah-freeman">Hannah Freeman</a></p>-->
</footer>

<style>
	#navbar {
		background-image: linear-gradient(90deg, var(--blue), var(--green));
		display: flex;
		color: white;
		width: 100%;
		height: 80px;
		text-shadow: 2px 2px 2px rgb(0, 0, 0, 25%);
		border-bottom: 2px solid black;
		-webkit-text-stroke: 4px black;
		paint-order: stroke fill;
		text-align: left;
		position: fixed;
	}

	#header-logo {
		display: flex;
		align-items: center;
	}

	#header-icon {
		margin: 6px 4px 2px 10px;
		width: 60px;
	}

	#header-title {
        font-size: 20px;
		letter-spacing: 5px;
		line-height: 20px;
    }

	#header-nav {
		display: flex;
		margin-left: auto;
	}

	footer {
		width: 100%;
		height: 80px;
		background-image: linear-gradient(90deg, var(--blue), var(--green));
		border-top: 2px solid black;
		position: relative;
		display: flex;
		justify-content: space-between;
		align-items: center;
	}

	#footer-links, #footer-socials {
		display: flex;
		margin: 0 10px;
	}

	#footer-links > a {
		color: white;
		text-decoration: none;
		margin: 10px 20px;
		font-weight: bold;
		font-size: 25px;
		paint-order: stroke fill;
		transition: 0.5s;
		-webkit-text-stroke: 4px rgba(1, 1, 1, 0);
	}

	#footer-links > a:hover {
		text-decoration: underline;
	}

	.social {
		height: 40px;
		margin: 0px 10px;
	}

	.social img {
		height: 40px;
	}

	#social-remind {
		color: white;
		text-decoration: none;
	}

	#social-remind > img {
		margin-top: -6px;
	}

	#remind-text {
		margin: -4px 0 0 0;
		font-size: 12px;
	}

	p {
		color: white;
	}
</style>
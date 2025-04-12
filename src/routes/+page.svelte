<head>
	<title>Hello | Jining Liu</title>

	<meta
		name="description"
		content="Hi 👋 I'm Jining, world's #1 procrastinator, Wii Sports enthusiast, and full stack student developer in Austin, TX."
	/>

	<meta property="og:url" content="https://jining.dev" />
	<meta property="og:type" content="website" />
	<meta property="og:title" content="Jining Liu" />
	<meta
		property="og:description"
		content="Hi 👋 I'm Jining, world's #1 procrastinator, Wii Sports enthusiast, and full stack student developer in Austin, TX."
	/>
	<meta
		property="og:image"
		content="https://opengraph.b-cdn.net/production/images/34467922-5607-4985-a46c-7a01c83cd5af.png?token=foCbBiemnuEhKz6X386FwvQJQdhljIu0904kXb2TPgM&height=450&width=800&expires=33280300900"
	/>

	<meta name="twitter:card" content="summary_large_image" />
	<meta property="twitter:domain" content="jining.dev" />
	<meta property="twitter:url" content="https://jining.dev" />
	<meta name="twitter:title" content="Jining Liu" />
	<meta
		name="twitter:description"
		content="Hi 👋 I'm Jining, world's #1 procrastinator, Wii Sports enthusiast, and full stack student developer in Austin, TX."
	/>
	<meta
		name="twitter:image"
		content="https://opengraph.b-cdn.net/production/images/34467922-5607-4985-a46c-7a01c83cd5af.png?token=foCbBiemnuEhKz6X386FwvQJQdhljIu0904kXb2TPgM&height=450&width=800&expires=33280300900"
	/>
</head>

<main class="vstack vcenter hcenter">
	<div class="hstack vcenter">
		<l1>Hello&nbsp;</l1>
		<l2 id="hand">👋</l2>
	</div>

	<div class="hstack vcenter">
		<l3 id="i-am">I'm&nbsp;</l3>
		<l3 id="name">Jining</l3>
	</div>

	<div id="nav" class="links vstack vcenter">
		<a class="internal" href="https://wii.jining.dev"> <p>Wii Stats</p></a>

		<a target="_blank" href="mailto:hello@jining.dev"> <p>Contact</p></a>

		<a target="_blank" href="mailto:business@jining.dev"> <p>Business</p></a>
	</div>

	<div id="socials" class="links vcenter hcenter">
		<a target="_blank" href="https://github.com/JiningLiu/"
			><img src="gh.png" alt="GitHub Logo" />
			<p>JiningLiu</p></a
		>

		<a target="_blank" href="https://bsky.app/profile/jining.dev"
			><img src="bsky.png" alt="Bluesky Logo" />
			<p>@jining.dev</p></a
		>

		<a target="_blank" href="https://www.youtube.com/@ItsJining"
			><img src="yt.png" alt="YouTube Logo" />
			<p>@ItsJining</p></a
		>
	</div>

	<div id="footer" class="hstack vcenter">
		<footer>© 2025&nbsp;&nbsp;</footer>
		<div></div>
	</div>
</main>

<style>
	main {
		height: calc(100% - 8% - min(10vw, 2rem));
	}

	#hand {
		transition-property: scale, transform;
		transition-duration: 0.2s;
	}

	#hand:hover {
		cursor: grab;
		scale: 1.2;
		transform: rotate(10deg);
	}

	#i-am {
		font-weight: 300;
	}

	#name {
		position: relative;
	}

	#name:hover {
		cursor: pointer;
	}

	#name::before {
		content: '';
		position: absolute;
		z-index: -1;
		width: 0;
		height: 8%;
		bottom: 2%;
		left: 2%;
		background-color: var(--primary-color);
		transition: all ease-in-out 0.1s;
	}

	#name:hover::before {
		width: 75%;
	}

	/* #name::after {
		content: '↗';
		opacity: 0;
		font-size: min(5vw, 3rem);
		font-weight: 400;
		position: absolute;
		left: 105%;
		bottom: 50%;
		transform: translate(0, 50%);
		transition: all ease-in-out 0.1s;
	}

	#name:hover::after {
		opacity: 1;
	} */

	.links {
		display: flex;
		flex-direction: row;
		margin-top: 4vh;
		gap: min(6vw, 1.8rem);

		@media (max-width: 600px) {
			&#socials {
				flex-direction: column;
				gap: min(2.4vh, 1rem);
			}
		}

		@media (max-width: 400px) {
			&#nav {
				flex-direction: column;
				gap: 0;
			}
		}

		a {
			opacity: 0.8;
			display: flex;
			flex-direction: row;
			align-items: center;
			position: relative;
			height: min(8vw, 2rem);
			gap: min(1.5vw, 0.4rem);
			color: var(--primary-color);
			text-decoration: none;
			transition: all ease-in-out 0.1s;

			img {
				width: min(8vw, 2rem);

				@media (prefers-color-scheme: dark) {
					filter: invert(1);
				}
			}
		}

		a:hover {
			opacity: 1;
		}

		a::after {
			opacity: 0;
			font-size: min(4vw, 1rem);
			font-weight: 400;
			position: absolute;
			bottom: 50%;
			transform: translate(0, 50%);
			transition: all ease-in-out 0.1s;
		}

		a:not(.internal)::after {
			content: '↗';
			left: calc(100% + min(4vw, 1rem) / 3);
		}

		a.internal::after {
			content: '↘';
			left: calc(-1.1 * min(4vw, 1rem));
		}

		*:hover::after {
			opacity: 1;
		}
	}

	#footer {
		opacity: 0.2;
		position: absolute;
		bottom: 8%;
		transition: all ease-in-out 0.2s;

		div {
			width: min(20vw, 4rem);
			height: min(10vw, 2rem);

			background-size: cover;
			background-image: url('/jl.png');
			@media (prefers-color-scheme: dark) {
				background-image: url('/jl_inverted.png');
			}
		}
	}

	#footer:hover {
		opacity: 1;
	}
</style>

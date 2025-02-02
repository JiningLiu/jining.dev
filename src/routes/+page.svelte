<head>
	<title>Hello | Jining Liu</title>
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

	<div id="links" class="vcenter hcenter">
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

	#links {
		display: flex;
		flex-direction: row;
		margin-top: 4vh;
		gap: min(6vw, 1.8rem);

		@media (max-width: 600px) {
			flex-direction: column;
			gap: min(2.2vh, 1rem);
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
			content: '↗';
			opacity: 0;
			font-size: min(4vw, 1rem);
			font-weight: 400;
			position: absolute;
			left: 105%;
			bottom: 50%;
			transform: translate(0, 50%);
			transition: all ease-in-out 0.1s;
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

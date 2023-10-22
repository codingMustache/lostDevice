<script>
	const buttons = {
		'contact.vcf': 'contact.svg',
		'mailto:contact@codingMustache.dev': 'email.svg',
		'https://github.com/codingMustache': 'github.svg',
		'https://www.linkedin.com/in/codingmustache/': 'linkedin.svg',
		'"tel:+14422646552"': 'phone.svg'
	}
</script>

<div class="main">
	<img
		class="pfp"
		src="pfp.png"
		alt="profile"
	/>
	<div class="buttons">
		{#each Object.entries(buttons) as [title, source]}
			{#if title === 'contact.vcf'}
				<a
					href={title}
					download="Jorge"
				>
					<button>
						<img
							src={'icons/' + source}
							alt=""
							width="50px"
							height="30px"
						/>
					</button>
				</a>
			{:else}
				<a
					href={title}
					target="_blank"
				>
					<button>
						<img
							src={'icons/' + source}
							alt=""
							width="50px"
							height="30px"
						/>
					</button>
				</a>
			{/if}
		{/each}
	</div>
	<span>👋</span>
	<div class="footer">
		<p>Hi I might have lost the thing you found I would love if you reached out and try to get them returned to me, thank you again.</p>
	</div>
</div>

<style>
	.footer {
		bottom: 0px;
		width: 100%;
		display: flex;
		align-items: center;
		padding: 10px;
	}
	.footer p {
		text-align: center;
	}
	span {
		font-size: xxx-large;
		display: flex;
		align-items: center;
		animation: wave 1s ease-in-out 0ms infinite;
	}
	@keyframes wave {
		0% {
			transform: rotateZ(-45deg);
		}
		50% {
			transform: rotateZ(90deg);
		}
		100% {
			transform: rotateZ(-45deg);
		}
	}
	.main {
		display: flex;
		width: 100%;
		max-width: 700px;
		flex-wrap: wrap;
		justify-content: center;
		height: 100vh;
		margin: 0 auto;
	}
	.buttons a {
		height: fit-content;
	}
	button {
		width: 100px;
		height: 50px;
		background-color: yellow;
		border-radius: 10px;
		border: 1px solid;
		box-shadow: inset 3px 3px rgba(255, 255, 255, 0.53);
		padding: 10px;
	}
	button:hover {
		box-shadow: inset 3px 3px 5px;
		cursor: pointer;
	}
	.buttons {
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		gap: 10px;
		width: 100%;
		padding: 10px;
		height: fit-content;
	}
	.pfp {
		object-fit: cover;
		width: 100%;
		height: 50vh;
		max-width: 700px;
		object-position: top;
		border-radius: 20px;
	}
</style>

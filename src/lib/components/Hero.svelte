<script>
	import profileImage from '$lib/assets/profile.webp';
</script>

<section class="hero" id="about">
	<div class="container">
		<div class="hero-content">
			<div class="profile-section">
				<img src={profileImage} alt="Profile" class="profile-image" />
				<div class="social-links">
					<a href="https://www.linkedin.com/in/valeria-li88/" target="_blank" rel="noopener noreferrer">
						<span>LinkedIn</span>
					</a>
					<a href="https://drive.google.com/file/d/1Q7LZD1qW0qz2LdCSPUmUodNLgSvElaAQ/view?usp=sharing" target="_blank" rel="noopener noreferrer">
						<span>CV</span>
					</a>
				</div>
			</div>
			<div class="about-content">
				<h1>Valeria Li <span class="pronunciation">/və.ˈlɛ.ɹi.ə ˈli/</span></h1>
				<h3>PhD Student in Hispanic Linguistics @ UPitt</h3>
				<p>
					I am a PhD student in Hispanic Linguistics at the University of Pittsburgh, advised by Dr. Marta Ortega-Llebaria and Dr. Scott F. Kiesling. My research interests include sociolinguistics, phonetics, and language variation.
				</p>
				<p>
					I graduated from Emory University in 2025 with a B.S. in Psychology & Linguistics, earning Highest Honors in Linguistics and completing my honors thesis on the linguistic structure and discursive roles of trauma dumping as a communicative action.
				</p>

				<!-- <p>
					<strong>Honors and Awards:</strong> Emory University Program in Linguistics - Award for Outstanding Leadership and Service; Charles Elias Shepard Scholarship; Emory Pathways Center Conference Grant
				</p> -->
			</div>
		</div>
	</div>
</section>

<style>
	.hero {
		padding: 4rem 0;
		scroll-margin-top: 4rem;
	}

	.container {
		max-width: 900px;
		margin: 0 auto;
		padding: 0 2rem;
	}

	.hero-content {
		display: flex;
		gap: 3rem;
		align-items: flex-start;
	}

	.profile-section {
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 1.25rem;
		min-width: 240px;
	}

	.profile-image {
		width: 240px;
		height: 240px;
		border-radius: 8px;
		object-fit: cover;
		background-color: #f1f5f9;
		border: none;
		transition: background-color 0.3s ease;
	}

	:global(main.dark) .profile-image {
		background-color: #1e293b;
	}

	.social-links {
		display: flex;
		gap: 0.75rem;
		flex-direction: column;
		width: 100%;
	}

	.social-links a {
		padding: 0.75rem 1.25rem;
		background-color: transparent;
		color: #0f172a;
		text-align: center;
		font-weight: 500;
		font-size: 1rem;
		border: 2px solid #0f172a;
		border-radius: 50px;
		transition: background-color 0.3s ease, color 0.3s ease;
	}

	.social-links a:hover {
		background-color: #0f172a;
		color: #f8fafc;
	}

	:global(main.dark) .social-links a {
		background-color: transparent;
		color: #f8fafc;
		border-color: #f8fafc;
	}

	:global(main.dark) .social-links a:hover {
		background-color: #f8fafc;
		color: #0f172a;
	}

	.about-content {
		flex: 1;
	}

	.pronunciation {
		font-size: 1.25rem;
		color: #64748b;
		font-weight: 400;
	}

	:global(main.dark) .pronunciation {
		color: #94a3b8;
	}

	@media (max-width: 768px) {
		.container {
			padding: 0 1.5rem;
		}

		.hero {
			padding: 3rem 0;
		}

		.hero-content {
			flex-direction: column;
			align-items: center;
			gap: 2rem;
		}

		.profile-section {
			width: 100%;
			max-width: 240px;
		}

		.about-content {
			text-align: left;
		}
	}
</style>

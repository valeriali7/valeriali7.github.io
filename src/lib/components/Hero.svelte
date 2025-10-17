<script>
	import profileImage from '$lib/assets/profile.jpg';
</script>

<section class="hero" id="about">
	<div class="container">
		<div class="hero-content">
			<div class="profile-section">
				<img src={profileImage} alt="Profile" class="profile-image" />
				<div class="social-links">
					<a href="https://www.linkedin.com/in/valeria-li88/" target="_blank" rel="noopener noreferrer">
						<svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
							<path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"></path>
							<rect x="2" y="9" width="4" height="12"></rect>
							<circle cx="4" cy="4" r="2"></circle>
						</svg>
						<span>LinkedIn</span>
					</a>
					<a href="https://drive.google.com/file/d/1Q7LZD1qW0qz2LdCSPUmUodNLgSvElaAQ/view?usp=sharing" target="_blank" rel="noopener noreferrer">
						<svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
							<path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"></path>
							<polyline points="14 2 14 8 20 8"></polyline>
							<line x1="16" y1="13" x2="8" y2="13"></line>
							<line x1="16" y1="17" x2="8" y2="17"></line>
							<polyline points="10 9 9 9 8 9"></polyline>
						</svg>
						<span>CV</span>
					</a>
					<div class="email-button">
						<svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
							<rect x="2" y="4" width="20" height="16" rx="2"></rect>
							<path d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7"></path>
						</svg>
						<span>val81@pitt.edu</span>
					</div>
				</div>
			</div>
			<div class="about-content">
				<h1>Valeria Li <span class="pronunciation">/və.ˈlɛ.ɹi.ə ˈli/</span></h1>
				<h3>PhD Student in Hispanic Linguistics @Pitt</h3>
				<!-- To delete paragraph, delete from <p> to </p> -->
				<p> 
					Hi! I'm Valeria, a PhD student in Hispanic Linguistics at the <a href="https://www.linguistics.pitt.edu/" target="_blank" rel="noopener noreferrer">University of Pittsburgh</a> advised by <a href="https://martaortegallebaria.com/" target="_blank" rel="noopener noreferrer">Marta Ortega-Llebaria</a> and <a href="https://sfkiesling.com/" target="_blank" rel="noopener noreferrer">Scott F. Kiesling</a>.
				</p>
				<p>
					My research primarily exists in the areas of Spanish language variation, sociophonetics, and discourse analysis. I am particularly interested in multilingualism in Latin America. I am also tangentially interested in the development and maintenance of virtual language and culture.
				</p>
				<p>
					I graduated from Emory University with a B.S. in Psychology and Linguistics with Highest Honors. My honors research was advised by <a href="https://linguistics.emory.edu/faculty/profiles/britt-erica.html" target="_blank" rel="noopener noreferrer">Erica R. Britt</a>, <a href="https://psychology.emory.edu/people/faculty/yamasaki-brianna.html" target="_blank" rel="noopener noreferrer">Brianna L. Yamasaki</a>, and <a href="https://www.ericakanesaka.com/" target="_blank" rel="noopener noreferrer">Erica Kanesaka</a> on discourse analysis of virtual language. I was also part of the <a href="https://babllab.com/" target="_blank" rel="noopener noreferrer">Brain, Behavior, and Broader Learning Laboratory</a> under Brianna L. Yamasaki where I conducted neuropsychological research on the intersection of multilingualism and cognitive behaviors and development such as executive function.
				</p>
				<p>
					Currently, I am an instructor of Spanish language at Pitt supervised by <a href="https://www.spanport.pitt.edu/people/dolores-lima" target="_blank" rel="noopener noreferrer">Dolores Lima</a>, teaching courses like SPAN 0103 Intermediate Spanish 3. At Emory, I was extensively involved with the <a href="https://writingcenter.emory.edu/index.html" target="_blank" rel="noopener noreferrer">Emory Writing Center</a> supervised by <a href="https://melissatyang.com/" target="_blank" rel="noopener noreferrer">Melissa T. Yang</a> and <a href="https://levinarnsperger.com/" target="_blank" rel="noopener noreferrer">Levin Arnsperger</a> where I worked as a writing consultant and English Language Learner instructor for ESL students.
				</p>
				<p>
					During my free time, I enjoy being indecisive over sweet treats and <a href="https://drive.google.com/drive/folders/1f-asKUhYbjSqp6ypb9Um-hOj8pRSzaw9?usp=drive_link" target="_blank" rel="noopener noreferrer">cooking</a> (especially for friends)!
				</p>
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
		position: relative;
	}

	.profile-section {
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 1.25rem;
		width: 240px;
		float: right;
		margin-left: 3rem;
		margin-bottom: 2rem;
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

	.social-links a,
	.email-button {
		color: #0f172a;
		font-weight: 500;
		font-size: 1rem;
		text-decoration: none;
		display: flex;
		align-items: center;
		gap: 0.5rem;
		transition: color 0.3s ease;
	}

	.social-links a:hover {
		color: #5470b3;
	}

	:global(main.dark) .social-links a,
	:global(main.dark) .email-button {
		color: #f8fafc;
	}

	:global(main.dark) .social-links a:hover {
		color: #7c96d9;
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
		color: #cbd5e1;
	}

	@media (max-width: 768px) {
		.container {
			padding: 0 1.5rem;
		}

		.hero {
			padding: 3rem 0;
		}

		.hero-content {
			display: flex;
			flex-direction: column;
			align-items: center;
			gap: 2rem;
		}

		.profile-section {
			float: none;
			margin: 0;
			width: 100%;
			max-width: 240px;
		}

		.about-content {
			text-align: left;
		}
	}
</style>

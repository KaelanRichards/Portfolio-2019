<template>
	<div class="author">

		<h1 v-if="showTitle" class="author__site-title">
			<!-- {{ $static.metadata.siteName }} -->
			Kaelan Richards.
		</h1>
		<h1 v-if="showTitle" class="author__site-title">
			<!-- {{ $static.metadata.siteName }} -->
			Indie Hacker.
		</h1>
		<h1 v-if="showTitle" class="author__site-title">
			<!-- {{ $static.metadata.siteName }} -->
			Founder.
		</h1>

		<p class="author__intro">
			Detroit-Native. Software Developer. Always striving to learn, grow, and create. 
		</p>

		<p class="author__links">
			<a target="_blank" rel="noopener noreferrer" href="https://www.instagram.com/detroitcoderboi/">Instagram</a>
			<a target="_blank" rel="noopener noreferrer" href="https://github.com/KaelanRichards">GitHub</a>
			<a target="_blank" rel="noopener noreferrer" href="https://twitter.com/kado_dev">Twitter</a>
		</p>

	</div>
</template> 
 
<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
export default {
	props: ['showTitle'] 
}
</script>

<style lang="scss">
.author {
	margin: 0 auto;
	max-width: 500px;
	text-align: center;
	padding-bottom: calc(var(--space) / 2);

	&__image {
		border-radius: 100%;
		width: 90px;
		height: 90px;
		margin-bottom: 1em;
	}

	&__intro {
		opacity: .8;
	}

	&__site-title {
		margin: 0 auto;
		font-size: 1.5em;
		max-width: 400px;
	}

	&__links {
		margin-top: -.5em;
		a {
			margin: 0 .5em;
		}
	}
}
</style>

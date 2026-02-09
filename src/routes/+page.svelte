<!--
@component
This is your page!
-->
<script>
  // Import all the news furniture components
  import ArticleHeader from '$lib/components/ArticleHeader.svelte';
  import ArticleBody from '$lib/components/ArticleBody.svelte';
  import Image from '$lib/components/Image.svelte';
  import RelatedLinks from '$lib/components/RelatedLinks.svelte';

  // Article metadata
  let headline = 'ok for some reason the last time i tried the npm install and run dev did not want to work, but i started over with a new repository and it was fine. .';
  let byline = 'Chloe Rogers';
  let pubDate = '2026-02-09';

  // Related stories
  const relatedStories = [
    { headline: 'How America\'s top news organizations escape rigid publishing systems to design beautiful data-driven stories on deadline.', href: 'https://palewi.re/docs/coding-the-news/' },
    { headline: 'How to install, configure and use Visual Studio Code, GitHub and Copilot', href: 'https://palewi.re/docs/coding-the-news/scripts/week-1/' },
    { headline: "How to publish a website with Node.JS and GitHub Actions", href:"https://palewi.re/docs/coding-the-news/scripts/week-2/"},
  ];
</script>

<!-- This sets the page title in the browser tab -->
<svelte:head>
  <title>{headline} | NYCity News Service</title>
  <meta name="description" content="i ran out of the prei" />
</svelte:head>

<!-- Your page content goes here -->
<div class="container">
  
  <!-- Article Header: Headline, byline, and publication date -->
  <ArticleHeader
    {headline}
    {byline}
    {pubDate}
  />

  <!-- Lead Image: Animated gif of students at the journalism school -->
  <Image
    src="/cat.jpg"
    alt="The Craig Newmark Graduate School of Journalism is at 219 West 40th Street in Midtown Manhattan."
    caption="The Craig Newmark Graduate School of Journalism is at 219 West 40th Street in Midtown Manhattan."
    credit="Craig Newmark Graduate School of Journalism"
  />

  <!-- Article Body: The main story text with proper typography -->
  <ArticleBody>
    <p>
      At the Craig Newmark Graduate School of Journalism at the City University of New York, change is in our DNA. That comes of being born in 2006, as the digital revolution was transforming our profession in ways none of us could have imagined.
    </p>

    <p>
      We fashioned a school to teach the latest storytelling, entrepreneurial, and technological skills alongside reporting, writing, and ethics. Beyond that, we’ve crafted a culture that spurns complacency, that isn’t afraid to pivot before the ground under us shifts.
    </p>

    <p>
      I also ran out of credits on Copilot. But I installed the Cline thing. 
    </p>

    

    
    </p>
  </ArticleBody>

  <!-- Related Stories: Links to other articles -->
  <RelatedLinks
    title="Related Stories"
    links={relatedStories}
  />

</div>

<style>
  /* Styles here only apply to this page */
  .container {
    padding: var(--spacing-lg) var(--spacing-md);
  }
</style>
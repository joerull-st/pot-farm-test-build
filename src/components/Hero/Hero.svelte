<!--
@component
### Hero component 
Renders a visual replica of the Immersive Template hero. 

#### Optional properties
- sectionLabel: string;
- headline: string;
- timestamp: string;
- heroImageUrl: string;
- heroImageCaption: string;
- heroImageAltText: string;
- dek: string;
- authorName: string;
- authorBioUrl: string;

#### Example
```svelte
<Hero
  sectionLabel = "Section label",
  headline = "Lorem ipsum dolor sit amet consectetur adipiscing elit",
  timestamp = "Dec. 1, 1977",
  heroImageUrl = "https://arc.stimg.co/startribunemedia/4SPNT7DI36ANT2SOB5N5EJAIJU.jpg",
  heroImageCaption = "",
  heroImageAltText = "",
  dek = "Lorem ipsum dolor sit amet consectetur adipiscing elit, fusce sociis at montes vitae tempor enim, venenatis tristique feugiat arcu dis ridiculus.",
  authorName = "Bryan Brussee",
  authorBioUrl = "https://www.startribune.com/bryan-brussee/8455834",
>
```
-->

<script>
  import Grid from "../Grid/Grid.svelte";
  import GridRow from "../Grid/_GridRow.svelte";
  import SectionLabel from "./_SectionLabel.svelte";
  import Headline from "./_Headline.svelte";
  import Timestamp from "./_Timestamp.svelte";
  import Image from "../Image/Image.svelte";
  import Dek from "./_Dek.svelte";
  import Byline from "./_Byline.svelte";

  /** @type {{sectionLabel?: string; headline?: string; timestamp?: string; heroImageUrl?: string; heroImageCaption?: string; heroImageAltText?: string; dek?: string; authorName?: string; authorBioUrl?: string;}} */
  let {
    sectionLabel = "",
    headline = "",
    timestamp = "",
    heroImageUrl = "",
    heroImageCaption = "",
    heroImageAltText = "",
    dek = "",
    authorName = "",
    authorBioUrl = "",
  } = $props();
</script>

<Grid additionalClasses="gap-y-8 md:gap-y-10">
  <!-- 
  <GridRow>
    <div class="flex justify-center my-6">
      <SectionLabel>{sectionLabel}</SectionLabel>
    </div>
    <div class="flex flex-col gap-y-6 md:gap-y-8 text-center">
      <Headline>{headline}</Headline>
      <Timestamp>{timestamp}</Timestamp>
    </div>
  </GridRow>

  {#if heroImageUrl}
    <GridRow variant={"fullBleed"}>
      <Image
        variant={"captionCentered"}
        src={heroImageUrl}
        alt={heroImageAltText}
        caption={heroImageCaption}
      />
    </GridRow>
  {/if}

  <GridRow
    additionalClasses="justify-self-center md:max-w-[535px] md:text-center lg:max-w-[712px]"
  >
    <div class="flex flex-col gap-y-5 md:justify-items-center md:items-center">
      <Dek>
        {dek}
      </Dek>
      <div class="flex items-center w-full gap-x-2 md:justify-center">
        <div class="flex flex-col gap-y-0.5 gap-x-1 md:flex-row">
          {#if authorName}
            <div class="flex">
              <Byline href={authorBioUrl}>By {authorName}</Byline>
            </div>
          {/if}

          <span class="text-text-secondary font-utility-label-reg-02">
            The Minnesota Star Tribune
          </span>
        </div>
      </div>
    </div>
  </GridRow> -->


<GridRow variant={"fullBleed"}>

<div class="relative flex items-center justify-center h-screen mb-4 overflow-hidden bg-[white] xl:max-h-[900px] lg:max-h-[850px] md:max-h-[700px] xs:max-h-[600px]">

  <div class="absolute md:left-4 md:bottom-2 xs:left-2 xs:bottom-2 z-30 xl:p-6 lg:p-4 md:p-4 xs:p-2 text-2xl !text-[white] text-left font-editorial-news-heading-01 max-w-[875px] mt-auto drop-shadow-md">
      <h1 class="xl:text-[4.5rem] lg:text-[4.5rem] md:text-[3.5rem] xs:text-[2.25rem] xs:whitespace-nowrap leading-[90%] mt-2">
        Take a look inside one of<br>Minnesota’s largest legal<br>marijuana harvests to date</h1>
  </div>

  
  <video autoplay="" loop="" muted="true" playsinline="" class="object-cover absolute h-full w-full">
      <source src="http://static.startribune.com/news/projects/all/2025-WEEDFARM-test/video%20files/pot_hero_3k_59fpsslowed.mp4?" type="video/mp4">Your browser does not support the video tag.
  </video>
</div>
</GridRow>



</Grid>

<Grid> 
  <GridRow variant={"inline"} additionalClasses={"gap-y-3"}>
<h2 class="w-full xl:w-[100%] font-editorial-non-news-heading-03 font-regular leading-title text-left mx-auto mt-20 xs:mt-10 pb-4 text-primary xl:text-3xl lg:text-2xl md:text-2xl xs:text-[22px]"><hr class="mb-3 w-[40%] border-x-0 border-t-0 border-b-4 border-b-[#00854B]">It’s “all hands on deck” for Prairie Island Indian Community’s fall cannabis harvest.</h2>


<div class="byline rt-Box contents items-center gap-x-2 max-w-2xl mx-auto font-utility-label-reg-02">
  <div class="rt-Box inline-block items-center gap-x-2">
    <div class="rt-Box w-full mb-3 inline-block items-center gap-x-2">
      <div class="rt-Box inline-block gap-y-0.5">
        <div class="rt-Box inline-block items-center">
            <p class="rt-Text font-utility-label-bold-02 text-text-primary relative mr-2">By <a class="!no-underline" href="https://www.startribune.com/author/matt-delong/6370469" target="_blank">Matt DeLong</a>, photos by <a class="!no-underline" href="hhttps://www.startribune.com/author/richard-tsong-taatarii/6370558" target="_blank">Richard Tsong-Taatarii</a></p>
        </div>
        <div class="rt-Text text-text-secondary font-utility-label-reg-02">The Minnesota Star Tribune</div>
      </div>
    </div>
    <div class="rt-Flex inline-block rt-r-display-flex rt-r-jc-start">
      <div class="rt-Text font-utility-label-reg-caps-03 text-text-secondary !text-[.6875rem] pb-8">November 21, 2025 at 8:00am</div>
    </div>
  </div>
</div>
</GridRow>

</Grid>


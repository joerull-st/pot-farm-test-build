<!-- 
@component
### ArticleBody component
This is a general workspace illustrating what an article body might look like if you use only the components included in this template.  
ArticleBody doesn't accept any props. All contents will need to be hand-placed by a designer directly inside this component.  
In this example, Grid and GridRow help establish the width of the article body's contents. 
Documentation included with those components and accessed by VSCode tooltip explains each component in greater detail.

#### State in this component
- innerWidth: int - pixel width of the viewport.
- isMobile: boolean - derived from innerWidth, true if less than 768 pixels
- isTablet: boolean - derived from innerWidth, true if between 768 pixels inclusive and 1024 pixels exclusive
- isDesktop: boolean - derived from innerWidth, true if greater than 1024 pixels inclusive

#### Using state in this component
You can use any of the three derived states to render different variants of a GridRow component reactively.
The following example uses a ternary to render an image edge-to-edge on mobile but inline otherwise.

#### Example
```svelte
  <GridRow
    variant={isMobile ? "fullBleed" : "inline"}
  >
    <Image
      src="https://arc.stimg.co/startribunemedia/4SPNT7DI36ANT2SOB5N5EJAIJU.jpg"
      alt="Descriptive alt text"
      caption="Caption tk tk tk"
    />
  </GridRow>
```
-->

<script>
  import Grid from "../Grid/Grid.svelte";
  import GridRow from "../Grid/_GridRow.svelte";
  import Subhead from "./_Subhead.svelte";
  import Paragraph from "./_Paragraph.svelte";
  import Image from "../Image/Image.svelte";
  import ScrollySection from "../Scrolly/ScrollySection.svelte";

  let innerWidth = $state(0);
  let isMobile = $derived(innerWidth < 768);
  let isTablet = $derived(innerWidth >= 768 && innerWidth < 1024);
  let isDesktop = $derived(innerWidth >= 1024);
</script>

<svelte:window bind:innerWidth />

<Grid additionalClasses={"gap-y-5"}>

  <GridRow variant={"inline"} additionalClasses={"gap-y-5"}>
    <Paragraph>NEAR HASTINGS, MINN. ― It’s just after 10 a.m. on a sunny and brisk fall morning in southeastern Minnesota’s farm country, a short distance from the Mississippi River bluffs. A crew of three men is hard at work harvesting the season’s bounty.</Paragraph>
    <Paragraph>But this is not your typical farm.</Paragraph>
    <Paragraph> Rather than rows of corn or soybean, this crop comes with names like Blueberry Muffin, Glue 31 and Platinum Lemon Cherry Gelato. The 13-acre fenced compound outside of Hastings is owned by the Prairie Island Indian Community, which operates the  <a
    href="https://www.islandpezi.com/"
    target="_blank"
    rel="noreferrer">Island Pězi marijuana dispensary</a> near Treasure Island Casino.</Paragraph>
    <Paragraph>As Minnesota’s cannabis industry gets up and running, both state officials and consumers are counting on tribal cannabis businesses to help meet some of the initial demand for legal marijuana. Until the first crops from state-licensed cultivators hit shelves, the tribal operations and the state’s two medical cannabis suppliers are the only game in town.</Paragraph>
    <Paragraph>Prairie Island’s autumn haul, easily one of the largest legal cannabis crops ever harvested in the state, could help with a supply bottleneck <a href="https://www.startribune.com/recreational-cannabis-weed-minnesota-medical-rise-green-goods/601479981/"
    target="_blank"
    rel="noreferrer">that has left some dispensaries with empty shelves and frustrated customers.</a></Paragraph> 
    <Paragraph>Mike Knoebel, head of cultivation for Good Steward – the company contracted by the tribe to manage the cannabis farm – estimated the total outdoor harvest could approach 2,000 pounds.</Paragraph>
  </GridRow>

  <GridRow variant={"fullBleed"}>
    <div class="md:max-w-6xl mt-8 mb-12 mx-auto px-2">
      <img class="block mb-2" src="https://arc.stimg.co/startribunemedia/PVK2IWPJ4BC3JGB7GZAQ44PXXA.jpg?dpr=2&amp;auto=format&amp;w=1280" alt="photo">
      <div class="caption font-utility-meta-reg-02 text-tertiary text-right md:w-[45%] mr-0 ml-auto xs:min-w-[250px]"><hr class="mr-0 ml-auto mb-2 pt-2 w-[40%] max-w-[250px] border-x-0 border-t-0 border-b-3 border-b-[#00854B]">Matt Knoebel, head of cultivation, right, and Zach Booth, left,  loads some Blue Dream harvest from one of the green houses where temps are maintained around 80 Fahrenheit in Hastings, Minn., on Monday, Oct. 20, 2025. We go behind the scenes for the fall harvest at Prairie Island Indian Community's Island Pezi cannabis cultivation facility.</div>
    </div>
  </GridRow>

  <GridRow variant={"inline"} additionalClasses={"gap-y-5"}>
    <Paragraph>Within weeks, a whole new crop will be planted in the eight greenhouses on the property.</Paragraph>
    <Paragraph>“Plants go in, plants go out,” Knoebel said. “It’s always changing.”</Paragraph>
    <Paragraph> In the facility’s main office, employees were buzzing with news that Prairie Island was moments away from becoming the third Minnesota tribe to sign <a
    href="https://mn.gov/ocm/assets/Cannnabis_Compact_Between_Prairie_Island_Indian_Community_And_Minnesota_tcm1202-710169.pdf"
    target="_blank"
    rel="noreferrer">a cannabis compact</a> with the state. The agreement allows the tribe to license up to eight retail stores, as well as additional cultivation and manufacturing facilities, outside of tribal lands.</Paragraph>
    <Paragraph>Ed Buck, chairman of the tribe’s cannabis commission, said he was excited about the development but declined to discuss any future plans. A tribal spokesman said Prairie Island hopes to begin wholesaling cannabis to state-licensed businesses soon.</Paragraph>

    <Subhead>‘Croptober’ harvest</Subhead>

    <Paragraph>Inside one of the greenhouses in mid-October, Zach Booth used shears to cut thick, green stalks of pungent, fruity and spicy Blue Dream plants filling one of three 86-foot-long garden beds.</Paragraph>

    <Paragraph>Booth broke the plants into manageable pieces that will hang dry for about 10 days in a large, climate-controlled storage room. Each greenhouse will produce 150 to 200 pounds of dried cannabis.</Paragraph>

    <Paragraph>“During ‘Croptober,’ it’s all hands on deck wherever they need you,” Booth said.</Paragraph>
  </GridRow>




  <GridRow variant={"fullBleed"}>
    <div class="md:max-w-6xl mt-8 mb-12 mx-auto px-2">
      <img class="block mb-2" src="https://arc.stimg.co/startribunemedia/QZ6SE4L6D5GVFI2RSQ4NVVD6BI.jpg?dpr=2&amp;auto=format&amp;w=1280" alt="photo">
      <div class="caption font-utility-meta-reg-02 text-tertiary text-right md:w-[45%] mr-0 ml-auto xs:min-w-[250px]"><hr class="mr-0 ml-auto mb-2 pt-2 w-[40%] max-w-[250px] border-x-0 border-t-0 border-b-3 border-b-[#00854B]">Zachariah Booth helps with the harvest in Hastings, Minn., on Monday, Oct. 20, 2025. We go behind the scenes for the fall harvest at Prairie Island Indian Community's Island Pezi cannabis cultivation facility.</div>
    </div>
  </GridRow>



  <GridRow variant={"inline"} additionalClasses={"gap-y-5"}>
    <Paragraph>In addition to the greenhouses, more than 2 acres were cultivated outside, in raised beds or 65-gallon containers filled with a proprietary soil blend.</Paragraph>
    <Paragraph>The entire operation employs nearly 40 people, including 14 enrolled tribal members, four of whom are in management, according to a tribal spokesman.</Paragraph>
    <Paragraph>In a greenhouse, Knoebel arranged harvested plants in plastic tubs as he explained the regenerative-farming philosophy at work.</Paragraph>
    <Paragraph>“These are what we call a no-till raised bed,” Knoebel said, pointing to the long canvas beds spanning the length of the greenhouse. “We won’t be disturbing the soil. The goal is to promote healthy microbiology in the soil.”</Paragraph>
    <Paragraph>The soil is made of mushroom compost, a custom blend of minerals, earthworm castings and rice hulls, all sitting atop a layer of oak logs. When leaves are pruned from the cannabis plants, they are simply dropped onto the soil to become food for worms, insects and fungi, just as they would be in nature.</Paragraph> 
    <Paragraph>“All the nutrients that were in those stems and leaves can return to the soil to be broken down and used again,” said Knoebel, who grew up in Wisconsin and spent about six years working in the legal cannabis industry in northern California.</Paragraph>
  </GridRow>



  <GridRow variant={"fullBleed"}>
    <div class="md:max-w-6xl mt-8 mb-12 mx-auto px-2">

      <div class="md:flex">
        <div class="mr-0 lg:w-1/3 md:w-full xs:w-full md:mr-2 xs:mr-0 xs:mb-2 md:mb-0">
          <div class="bg-no-repeat bg-cover bg-top h-[38rem] xl:h-[38rem] lg:h-[38rem] md:h-[38rem] mb-0  xs:h-[40rem]" style="background-image: url('https://arc.stimg.co/startribunemedia/KVGD76YZTFDI3HX3BQ25CNTW44.jpg?dpr=2&auto=format&w=1280');"></div>
        </div>

        <div class="md:ml-0 lg:w-2/3 md:w-full xs:w-full xs:ml-0">
          <div class="bg-no-repeat bg-cover bg-top h-[38rem] xl:h-[38rem] lg:h-[38rem] md:h-[38rem] mb-0  xs:h-[25rem]" style="background-image: url('https://arc.stimg.co/startribunemedia/4USDGWOWVVHSLMJEV6CMJAI2SI.jpg?&w=712');"></div>
        </div>
      </div>

      <div class="caption font-utility-meta-reg-02 text-tertiary text-left md:w-[45%] text-right mr-0 ml-auto xs:min-w-[250px]"><hr class="mr-0 ml-auto mb-2 pt-4 w-[40%] max-w-[250px] border-x-0 border-t-0 border-b-3 border-b-[#00854B]">GROUP CAPTION HERE</div>
    </div>
  </GridRow>



  <GridRow variant={"inline"} additionalClasses={"gap-y-5"}>
    <Subhead>Underground experience</Subhead>
    <Paragraph>The vision for the operation’s sustainable practices comes from Good Steward CEO Tri Trong Nguyen,cq a 50-year-old Rochester native who spent years growing cannabis in Colorado.</Paragraph>
    <Paragraph>Nguyen made headlines in 2015 when he was indicted as the ringleader of <a
      href="https://www.startribune.com/operation-golden-gofer-busts-historic-colo-minnesota-pot-pipeline/297691711"
      target="_blank"
      rel="noreferrer">a 32-person smuggling operation</a> that used vehicles and sky-diving planes to ship up to 400 pounds of marijuana per month from Colorado to Minnesota.</Paragraph>
    <Paragraph>Nguyen was initially sentenced in 2017 to 11 years for trafficking and money laundering. However, when his sentence was revised by the courts four months later, he was released and placed on probation, according to court documents. He declined to be interviewed for this article.</Paragraph>
    <Paragraph>Nguyen’s story highlights a reality for Minnesota’s nascent legal cannabis industry: Many of the most experienced and sought-after cultivators gained their experience in the black market and may have complicated legal histories. </Paragraph>
    <Paragraph>In a statement, Prairie Island’s cannabis company CBH Inc. said Nguyen and his company were thoroughly vetted before licensing. The partnership dovetails with the company’s support of social equity efforts and “non-discrimination against those disproportionately affected by prior marijuana prohibition,” the company said.</Paragraph>
  </GridRow>




  <GridRow variant={"fullBleed"}>
    <div class="md:max-w-6xl mt-8 mb-12 mx-auto px-2">
      <img class="block mb-2" src="https://arc.stimg.co/startribunemedia/HZAZLDJLNJGOJHMBG6RWA35FEE.jpg?dpr=2&amp;auto=format&amp;w=1280" alt="photo">
      <div class="caption font-utility-meta-reg-02 text-tertiary text-right md:w-[45%] mr-0 ml-auto xs:min-w-[250px]"><hr class="mr-0 ml-auto mb-2 pt-2 w-[40%] max-w-[250px] border-x-0 border-t-0 border-b-3 border-b-[#00854B]">Laurie Murray takes a cutting from a cannabis plant in Hastings, Minn., on Tuesday, Sept. 9, 2025. We go behind the scenes for the fall harvest at Prairie Island Indian Community's Island Pezi cannabis cultivation facility.</div>
    </div>
  </GridRow>



  <GridRow variant={"inline"} additionalClasses={"gap-y-5"}>
    <Subhead>Year-round growth</Subhead>
    <Paragraph>Due to Minnesota’s notoriously short growing season, Knoebel said the greenhouses will operate throughout the winter. They are outfitted with grow lights, heaters and ventilation equipment, allowing four or five harvests per year. </Paragraph>
    <Paragraph>Once the greenhouses are empty, the soil will be re-amended and promptly filled with a new batch of plants started from thousands of cuttings from “mother” plants.</Paragraph>
    <Paragraph>“Because they’re genetic replicas, they’ll be 100 percent the same,” Knoebel said. “That way the product is always the same.”</Paragraph>
  </GridRow>



  <GridRow variant={"fullBleed"}>
    <div class="md:max-w-6xl mt-8 mb-12 mx-auto px-2">

      <div class="md:flex">
        <div class="mr-0 lg:w-1/2 md:w-full xs:w-full md:mr-2 xs:mr-0 xs:mb-2 md:mb-0">
          <div class="bg-no-repeat bg-cover bg-top h-[38rem] xl:h-[38rem] lg:h-[38rem] md:h-[38rem] mb-0  xs:h-[25rem]" style="background-image: url('https://arc.stimg.co/startribunemedia/VPJ2NFJK2ZGGVPRIT7RL6IXLXY.jpg?&amp;w=712');"></div>
        </div>

        <div class="md:ml-0 lg:w-1/2 md:w-full xs:w-full xs:ml-0">
          <div class="bg-no-repeat bg-cover bg-top h-[38rem] xl:h-[38rem] lg:h-[38rem] md:h-[38rem] mb-0  xs:h-[25rem]" style="background-image: url('https://arc.stimg.co/startribunemedia/LY4BJ3T545FNBD2ZIY4HX3GMSQ.jpg?&amp;w=712');"></div>
        </div>
      </div>

      <div class="caption font-utility-meta-reg-02 text-tertiary text-left md:w-[45%] text-right mr-0 ml-auto xs:min-w-[250px]"><hr class="mr-0 ml-auto mb-2 pt-4 w-[40%] max-w-[250px] border-x-0 border-t-0 border-b-3 border-b-[#00854B]">GROUP CAPTION HERE</div>
    </div>
  </GridRow>


  <GridRow variant={"inline"} additionalClasses={"gap-y-5"}>
    <Paragraph>Cannabis plants are also grown year-round in indoor vegetative and flowering rooms.</Paragraph>
    <Paragraph>The temperature and humidity are kept high to encourage rapid growth in the “veg” rooms, where the plants are stacked from floor to ceiling to maximize growth. The plants are eventually moved to a flowering room, where the amount of light they receive is increased while the air cooled and the humidity lowered, to stave off the development of mold or the dreaded botrytis fungus, also known as bud rot.</Paragraph>
    <Paragraph> In an office in the compound’s main building, the entire operation is mapped and tracked using computer software. Every one of the nearly 9,000 plants at the facility must be tagged with a bar code. </Paragraph>
    <Paragraph>Randi McDonald, who oversees METRC, the tribe’s “seed-to-sale” cannabis tracking system, uses spreadsheets and color-coded maps to track the growth stages of plants in the indoor grow rooms, greenhouses and outdoor areas. When plants are moved from one place to another, she updates her maps.</Paragraph>
    <Paragraph>“It’s a lot,” she said. </Paragraph>

    <Subhead>Moving the product</Subhead>

    <Paragraph>After the plants have dried to an ideal moisture content, flowers will be stripped from the branches and run through one of two trimming machines that remove any remaining leaves and automatically sort them by size before they are packaged.</Paragraph>

    <Paragraph>Any buds not deemed suitable for sale as premium flower will move to an on-site manufacturing facility operated by a different company, North Star Canna, to be turned into joints and other products.</Paragraph>
  </GridRow>


  <GridRow variant={"fullBleed"}>
    <div class="md:max-w-6xl mt-8 mb-12 mx-auto px-2">

      <div class="md:max-w-6xl mt-2 mb-0 mx-auto px-0">
        <img class="block mb-2" src="https://arc.stimg.co/startribunemedia/4T6LVR4JMZFWFPL57LJNMU4UIE.jpg?dpr=2&amp;auto=format&amp;w=1280" alt="photo">
      </div>


      <div class="md:flex">
        <div class="mr-0 lg:w-1/2 md:w-full xs:w-full md:mr-2 xs:mr-0 xs:mb-2 md:mb-0">
          <div class="bg-no-repeat bg-cover bg-center xl:h-[28rem] lg:h-[28rem] md:h-[28rem] mb-0  xs:h-[20rem]" style="background-image: url('https://arc.stimg.co/startribunemedia/XNXQ3XMDZJDEFG7HRSTBI2USTE.jpg?&amp;w=712');"></div>
        </div>

        <div class="md:ml-0 lg:w-1/2 md:w-full xs:w-full xs:ml-0">
          <div class="bg-no-repeat bg-cover bg-center xl:h-[28rem] lg:h-[28rem] md:h-[28rem] mb-0  xs:h-[20rem]" style="background-image: url('https://arc.stimg.co/startribunemedia/3OM7VUCJFRD33FXGTYRJS6CCMI.jpg?&amp;w=712');"></div>
        </div>
      </div>

      <div class="caption font-utility-meta-reg-02 text-tertiary text-left md:w-[45%] text-right mr-0 ml-auto xs:min-w-[250px]"><hr class="mr-0 ml-auto mb-2 pt-2 w-[40%] max-w-[250px] border-x-0 border-t-0 border-b-3 border-b-[#00854B]">GROUP CAPTION HERE</div>
    </div>
  </GridRow>



  <GridRow variant={"inline"} additionalClasses={"gap-y-5 pb-10"}>
    <Paragraph>A sample of every batch that goes out the door is tested for potency and contaminants like mold or pesticides. Now that the tribe has signed a cannabis compact allowing off-reservation sales, all testing will be done by state-licensed facilities, said Good Steward’s Chief Operating Officer Johnny Murray. </Paragraph>
    <Paragraph>“Everything tracking into the state must follow [Office of Cannabis Management] testing standards,” he said.</Paragraph>
    <Paragraph>At the Island Pězi dispensary, the prized top buds will be sold as premium cannabis flower, currently fetching more than $400 an ounce. </Paragraph>
  </GridRow>

</Grid>

<style>
  a {
    text-decoration-line: underline;
    text-decoration-color: #00854b;
    text-underline-offset: 2px;
  }

  a:hover {
    color: #00854b;
  }
</style>

---
layout: default
title: Grounding and Lightning Protection
categories: 
created: 2013-07-30
changed: 2013-08-05
post_author: critzo
lang: fr
---
<h2>Introduction</h2>

<p>This is a companion to the <a href="/docs/build/roof-mount-guide">Rooftop Mounting Guide</a>, where we discuss installing an antenna your roof. Of course, when you install any metal pole on your roof, you are creating a lightning rod! Lightning can be very damaging, so we want to make sure we protect against it. It is important to note that if your house or building isn’t the highest thing in the area - for instance if there are tall trees close by or if there are other taller buildings around - your risk of actually being struck by lightning is <strong>extremely small</strong>. Keep this in mind, and don’t panic about putting up an antenna mast! If you follow a few of these steps here you can protect yourself from damage to your home or electronics. Though lightning is dangerous, it is extremely unlikely to be struck. A more common problem is static build-up from electric charge in the air during a lightning storm. This static can cause a charge to run down the cables from the roof and damage equipment in your house. We want to direct this charge in to the ground, rather than in to your electronics!</p>

<h2>What to ground to?</h2>

<p><img alt="" class="img-responsive" src="/files/styles/large/public/existing_ground_rod.jpg?itok=cXG2JCPu" style="width: 400px; height: 300px; float: right; margin: 5px;" typeof="foaf:Image" />Before we talk about what to install, we should talk about what qualifies as ground. There are lots of options, but there are three safe ones:</p>

<ul>
	<li>An existing ground rod, tied to your electrical panel.</li>
	<li>The water utility pipe that enters the building.</li>
	<li>A new ground rod that you drive yourself.</li>
</ul>

<h3>Using an existing ground rod</h3>

<p>You should already have a ground rod in or just outside of your house. It will be very close to your electrical panel - either under it in the floor of the basement, or outside of the house where the electrical cable comes in from the utility. You can use this ground rod, as long as it is relatively close to the antenna mast you are installing. If the mast is on the other side of the house, or more than 20 feet or so away along the ground, another grounding point might be better.</p>

<h3>Using the cold water pipe</h3>

<p><img alt="" class="img-responsive" src="/files/styles/large/public/incoming_water_pipe.jpg?itok=TPbEdMeN" style="width: 300px; height: 400px; float: right;" typeof="foaf:Image" />If the pipe that supplies water to your house is made of copper or some other metal, you can use it as a ground. Most likely the only way to access this pipe is in the basement or crawl space of your house. They do not typically come in to the house above ground, to prevent your pipes from freezing. Typically the water meter is installed immediately after this pipe comes in the building - on the side of the house closest to the street. Your electrical panel might already be grounded to this pipe - you might be able to follow the copper wire coming out of the bottom of the panel. Again, you can use this pipe as a ground conductor, as long as it is close to where the antenna mast is located on the roof. If it is on the other side of the house, this may not work.</p>

<p>&nbsp;</p>

<h3><img alt="" class="img-responsive" src="/files/styles/large/public/grounding_rod_clamp.jpg?itok=nYwgOpfb" style="width: 400px; height: 251px; float: left; margin: 5px;" typeof="foaf:Image" />Installing a new ground rod</h3>

<p>(Note: You will need two people, a small A-Frame ladder and a small sledge hammer for this.) If you don’t have any other options, you will need to drive a new ground rod. Pick a spot on the ground directly below your antenna mast. To make it easy on yourself, it should be softer soil, not rocky ground - and certainly not concrete or asphalt. Make sure to start at least a foot or 18” away from the edge of the house - the concrete or brick footer of the house can sometimes extend out nearly that far. If you want the new ground rod to be hidden from view, dig a small pit where you intend to put the rod. You can then fill in the soil over the rod when you are finished. Pick the spot on the ground where you want to place the rod, and have a partner hold the rod upright. Since ground rods are typically 8 feet long, you will need a small ladder to reach the top of the rod. Then, carefully (so as not to hit your partner!) hammer the top of the rod with a 5 pound hammer or small sledge hammer. As the rod is driven down, you may need to descend the ladder for the best angle to drive it. Once the rod is within a few inches of the ground, you can stop.</p>

<h2>What NOT to ground to?</h2>

<p>There are a few things that you shouldn’t ground to in your home:</p>

<ul>
	<li>The gas pipe, or gas meter.</li>
</ul>

<p>The gas line from the utility is not a good ground - it can’t be trusted.</p>

<p>Even if there is a copper wire running to the meter, don’t use it - that wire is just to bond it to the real ground elsewhere in the building.</p>

<ul>
	<li>Metal beams, or exposed metal reinforcing.</li>
</ul>

<p>These are typically made of iron or steel, and it is very difficult to determine if they provide a ground, so they can’t be trusted.</p>

<h2>So what do I really need?</h2>

<p>There are a few options for how to install lightning protection: a wire from the antenna mount to a grounding source (described below), or a surge arrester.</p>

<p>How to decide? Generally, if you have a metal antenna mount on your roof that is over 5 feet tall, you will want to ground that using a long copper wire. If the mount is shorter, or doesn’t rise above the roof line, then you can just use a surge arrester. Even if you aren’t grounding the hardware on the roof, and just using a surge arrester, that arrester will need to be grounded. This is typically easier, as it can be done at ground level, and done near an existing ground to make wiring easier.</p>

<h2>Installing a Surge Arrester</h2>

<p><img alt="" class="img-responsive" src="/files/styles/large/public/surge_arrester_in-line_diagram.png?itok=TtsY-WHn" style="width: 316px; height: 423px; float: right;" typeof="foaf:Image" />You have likely already used a surge arrester - they are sometimes built in to multiple outlet power strips. They function by preventing a surge (quick build-up) of electrical energy from entering your appliances. This surge is shunted or directed to ground instead - either the large round pin on the wall plug (in the case of a power strip), or with a copper or aluminum wire if you are grounding outdoor equipment. You will want to install a surge arrester on the Ethernet cable that connects from the wireless Router on your roof to your indoor Access Point or computer. In order to do this, we will actually need to create two Ethernet cables: one that runs from the rooftop Router to the surge arrester, and one that runs from the arrester to the indoor unit. The surge arrester is grounded by running a #10 AWG copper or aluminum wire from a metal lug inside of the arrester to one of the grounding connections mentioned above. There are many models of surge arrester available, but unfortunately aren't likely available in local hardware stores. We need special surge arrestors that mount outdoors, and allow power from the Power over Ethernet adapter to reach the router. L-Com is a good source for buying them on-line:</p>

<ul>
	<li>http://www.l-com.com - Search for part number AL-CAT5EJW24 or AL-CAT6JW</li>
</ul>

<p><img alt="" class="img-responsive" src="/files/styles/large/public/outdoor_surge_arrestor.jpg?itok=Y4k9Cgr-" style="width: 250px; height: 165px; float: right;" typeof="foaf:Image" />The outdoor arrestor should be installed directly below the rooftop Router, as close to the ground as possible. This is to minimize the length of wire between the arrestor and the ground rod or ground conductor, since they should be installed in the ground or in the basement. It should mount with two short screws to the wood, concrete or brick base of the building.</p>
 

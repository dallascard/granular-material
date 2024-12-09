---
title: "Bespoke Navigation"
date: 2024-09-29T16:51:57-04:00
draft: false
tags: [maps,street-view,measurement,visualization,software,knowledge-infrastructure,large-language-models,bikes]
---


I don't normally do this, but I recently did a short bike trip in Michigan, and I thought I would write a brief post about it, in part because it cued various other ideas which have a more direct connection to the kinds of things I normally write about here.

<!--more-->

The trip itself can be described succinctly. When a larger trip that I had planned with friends fell through, I decided to salvage the situation by doing a quick one-night solo tour. Starting in Ann Arbor, I took the Amtrak to Kalamazoo, and then rode from there to Saugatuck, on the coast of Lake Michigan. My route was mostly along the Kal-Haven trail, which connects Kalamazoo and South Haven, and then from there up the coast another twenty miles or so. I spent one night in Saugatuck, with just enough time to see a bit of the town, and then rode back to Kalamazoo the next day.

Although just putting in the miles and being in motion all day are sufficient rewards in themselves to justify the trip, it's also tremendous fun to explore and have the experience of traversing the space.[^1] In this case, an unexpected highlight ended up being a little Mexican food truck and grocery store in Grand Junction that a friend of a friend recommended.[^2] It was kind of surreal to find such a place in what felt, to me, like the middle of nowhere, but it was a total delight. In addition to some very good tacos, I also got what I'd say was the best tamale I've ever had.[^3]
 
Overall, the Kal-Haven trail was quite impressive.[^4] It's about 40 miles long, paved in a few places, but mostly dirt or gravel. It's also in a forest corridor almost the whole way, which makes it quite beautiful for riding. That kind of dedicated trail is obviously a much safer alternative to riding on roads, since there are no cars to worry about, except at the occasional road crossing. On the other hand, it did get a little bit monotonous after a while, as there isn't all that much variation in scenery, nor any particularly exciting places to stop. The infrastructure was great, with pretty frequent outhouses along the way, plus a few water pumps and bicycle tools, which are a very nice bonus. Overall, the maintenance was quite good, although in a few places people had added some very sand-like gravel fill that was not great for riding.

{{< figure src="/img/bespoke-navigation/kalhaven.jpg" >}}

For trips like this, it has become entirely routine to rely on Google maps for route planning. A lot of the best bicycle tours I've done have followed very standard routes, such as the Erie Canal trail, and in those cases, it's really just a question of finding places to eat or sleep. Going off of such conventional routes requires a bit more research. In this case, I chose my destination partly based on what was feasible from an Amtrak station, and what seems suitable for biking, but that still opens up a lot of possibilities. Especially for cycling, small differences in road quality, like the width of the shoulder, or how heavy the traffic is, can make a huge difference in terms of how safe and enjoyable a ride feels. Getting stuck on a high speed, high traffic road with no shoulder for an extended ride is something to be avoided at almost any cost.

Unfortunately, the support for bike trip planning on Google maps is still somewhat limited, if nevertheless helpful. The most obvious relevant feature is the optional Biking layer, which adds markings to indicate how bike friendly a road is. I had thought there were only two types of lines, but it turns out there are actually [four or five](https://support.google.com/maps/answer/3092439?hl=en&co=GENIE.Platform%3DDesktop#zippy=%2Cbiking-trails), depending on how you count. Dark green lines represent trails that don't have car traffic (such as the Kal-Haven trail). Lighter green lines represent (at least in theory) "roads that are shared with cars and have a separate bike lane". If you zoom in farther, you can also see dotted green lines, which represent "bicycle-friendly roads", which don't have bike lanes but are nevertheless recommended for cyclists. Apparently there are brown lines for unpaved dirt trails, although I'm not sure I've ever noticed these. Finally, some of the green lines are dashed, rather than solid, but I'm not clear on what that means. My understanding is that this information is at least partially crowd sourced (possibly with some sort of base layer or image analysis?), but there doesn't seem to be a lot of information available about how this information is sourced or aggregated.

These markings are a great start, but are far from a complete solution. Anything shown to be a dedicated lane (solid line) generally seems to be pretty reliable, but there is wide variation in what such routes might be, from a true physically separated bike lane, to a wide shoulder with share-o symbols printed on the road. Moreover, it's rare to find solid green lines that extend continuously for any meaningful distance so it's often a question of stitching together multiple pieces, while trying to avoid the least pleasant conditions.

Bicycle-friendly roads (dotted lines) are much even more variable, and hard to rely on, in part because that classification might only apply going in a single direction, which is not clearly marked on the map interface. One can try to figure out such restrictions by using Google's suggested navigation directions, (which will be different for bicycle travel than for other types of transportation), but there are lots of other reasons why Google might suggest or fail to suggest a route, and it's not easy to customize such suggestions to one's preferences. For bicycling, in particular, Google maps tries to keep you riding in strictly legal ways, and so will avoid, for example, routing you the wrong way down a one way road. This is reasonable, but it can sometimes ignore a possibility as simple as just crossing the road, or riding on the sidewalk. On this particular trip, I also got fooled by Google directions in a classic way. Trying to get to downtown Saugatuck, it sent me on a route across the lake, which I assumed was a bridge. Only when I got there did I realize that it was actually a ferry that was now closed for the season. Welp.

{{< figure src="/img/bespoke-navigation/ferry.jpg" >}}

In the case of my most recent trip, the Kal-Haven trail was a combination of solid and dashed lines, although it was essentially just a single trail the whole way, so I'm not sure why it isn't just a solid line, but perhaps it has to do with the quality of the trail in different places. For heading up the coast, I took the Blue Star Highway, which was marked as a bicycle-friendly road (dotted line). This was broadly true, as there was a decent shoulder most of the way. But it was also a pretty high speed and high traffic road, and not necessarily the most pleasant to ride on.

That naturally leads into the second key feature of Google maps, which is [Street View](https://www.google.com/streetview/). I've been thinking a lot lately about how crazy it is that Street View exists, and that it's possible to view photographs of so much of the planet via the maps interface. Overall, it feels like we haven't yet grappled with the profound cultural influence of Street View, and can imagine writing  more about this kind of thing in the future. In the meantime, however, I will just mention that Street View is possibly *the* most useful feature for this kind of trip planning. Although it is a lot more work, it is the best way to get more detailed information about what a route would be like to ride on. For this trip, checking out some images of Blue Star Highway along the route before leaving home was great for giving me some confidence that it would be relatively safe to ride on.

That being said, I didn't end up loving the route, in part due to the high traffic volume. So, for the ride home, I decided to try something different. I had a bit of extra time in Saugatuck, so I decided to see if I could come up with an alternate route home by doing some extensive exploration of Street View images in the area between Highways 40 and 196. There are basically no green lines anywhere in this area, except for some trails near Swan Creek Marsh, so it required a lot of dragging the little orange person onto the map over and over again.

{{< figure src="/img/bespoke-navigation/screenshot.png" >}}

Ultimately, it's actually a lot easier to rule roads out than to rule them in. Many roads have no shoulder at all, which are easily vetoed. Others are just dirt roads, which are okay, but I would generally prefer to ride on pavement. Others look like they are just in such rough shape in terms of maintenance that they would not be pleasant to ride on. The challenge of course is knitting together enough sections to find a continuous route from point A to point B. In the end, I settled on taking 56th street through Fennville down to Grand Junction, and then rejoining the trail there. Overall that route was much more satisfying that the route that Google had previously given me. Probably 95% of it was on perfect newly paved roads with a generous shoulder and not much traffic. Maybe 4% was rougher pavement or similarly worse conditions. And then at the very end I was briefly stuck on a very bumpy dirt road that was a bit unpleasant. But overall, it was awesome, not just for better riding conditions, but also for the sense of exploration and adventure.

{{< figure src="/img/bespoke-navigation/backroads.jpg" >}}

That all got me thinking that there must be a better way. I haven't yet explored many of the possibilities, but it does seem like there are numerous other tools out there that people use for bike trip route planning, from looking at Strava heat maps (to find popular routes), to specialized apps like [Komoot](https://www.komoot.com/).[^5] I expect there could be value here, but it also feels like this is a case where a more customized solution might be needed. Personal preferences will factor in a lot, and someone else's preferred route might be quite different from mine.

Really what I want is to be able to use Street View imagery (or other similar resources) to classify roads in terms of how nice they would be for riding in each direction, and then somehow combine this with Google's information about impassible routes, or other relevant information. That is, considering things like speed limit, traffic patterns, shoulder width, pavement quality, and so on, it would be awesome to generate a map that colours roads as being acceptable for riding in one direction, the other direction, or both. I'm not sure yet how much of this information is available through the google maps API or something like OpenStreetMap, but it feels like it might be fun to try to build! Previously, I would have assumed that this would be far enough outside of my expertise that it would take me forever to attempt such a thing. But with the degree to which LLMs have unlocked the ability to work with unfamiliar interfaces and modules, this feels like it could be easily worth trying.

Overall, I guess the message here is twofold. First, I feel like we still have not fully reckoned with just how remarkable it is that geographic information is now so widely available, and the cultural influence of Google maps more broadly, especially Street View. Second, that fact notwithstanding, we are also clearly in the midst of another revolution, which is the degree to which it has now become relatively trivial to build at least somewhat sophisticated software for custom purposes. I think most of us have gotten so used to having to put up with crappy software that defies our preferences and is perpetually [unstable](https://dallascard.github.io/granular-material/post/stability/), that we've perhaps lost the instinct to ask for better. It's probably optimistic, but it does feel like there is a fair bit of untapped potential here for better designing our own worlds. Of course, I haven't actually tried to build my custom system for bicycle route planning yet, but based on other experiments, I suspect that it wouldn't be that hard. What this means in terms of customizability, centralization, or fragmentation remains to be seen, but I am definitely excited to see what kinds of experiments come from this.


{{< figure src="/img/bespoke-navigation/saugatuck.jpg" >}}


[^1]: With this trip complete, I have now ridden fully across the Mitten, in pieces, from East to West.

[^2]: If you're in the area, the place is called [E&L Sazon Oaxaqueno](https://maps.app.goo.gl/S2E71DMLMS4yRsxC6), and I highly recommend it!

[^3]: Admittedly, all food tastes better on bike trips, but even so.

[^4]: Technically what I'm describing is a combination of a couple of different trails, including the actual segment called the Kal-Haven trail, but I'm just going to call the whole thing that for the sake of simplicity.

[^5]: If anyone's had good experiences with these options or knows of other better ones, I'd definitely be interested to hear about it!

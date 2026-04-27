---
title: "Assignment 2: Manual Geocoding vs Automated Geocoding"
excerpt_separator: "<!--more-->"
categories:
  - Assignment
tags:
  - assignment
  - openstreet
  - map
  - r
---

## Assignment Documentation and Reflection
### Context research
We briefly looked at the context of the text in order to understand it a bit better, which would help us later in the manual geocoding process. Notes on contextual research: Theodore and Mabel Bent, married in 1877, went on frequent journeys together, documenting their experiences along the way. Their travels continued for around 20 years until Theodore died in 1897 from malaria. Despite this, Mabel continued preserving the memories of their shared adventures in notebooks she had written during their trips. In 1929, their journey accounts, otherwise known as their Chronicles, found their way into the archive of the Hellenic Society.

### Manual geocoding process on Recogito
Through the use of Recogito, it was surprising to see how many locations could be registered, as well as those that could not be found. From the beginning, it became clear that the places that were easier to locate were countries. For example, Recogito easily identified mentions of England, Africa, Arabia, and Syria, among others. Then, there were the places that, despite having slightly lesser-known or outdated names, were still identified by the system, such as Aden, Hadhrami (recognized as Hadramawt in Yemen), Maskkat (recognized as Muscat in Oman), Hindustani, or Shibahm. 

<figure>
  <img src="{{ '/assets/images/makalla.png' | relative_url }}" alt="Screenshot of Recogito">
</figure>

*the different variations of Makalla in Recogito*

Nonetheless, even though Recogito recognized these places, it struggled to identify more specific locations within them. Makalla was one of the places we struggled the most to locate, as it appeared under different names in the GeoNames search bar. The closest match suggested that it was most likely Al Mukalla. Similarly, another location we struggled to locate was “Mareb”, whose closest association appeared to be“Ma’rib” in Yemen.

If a place has one or two name variations, Recogito would still be able to recognize it (example: Muscat and Maskat). However, like Muscat, many of the locations Recogito was able to identify are popular, big cities (or a continent/region/country). With small or historical locations like the Wadis, it struggles a bit more. During this process, we had to manually look up the latitude and longitude of these places on Google, using websites like GeoNames or Geoviews (ye.geoview.info) to obtain the data. This raised some questions regarding what makes a location more identifiable within Recogito. For instance, if a place is located manually and its coordinates are inserted as a comment when highlighting it, does this help the system recognize and retain that location for future texts evaluated on the platform? Additionally, the variation and evolution of place names raises further uncertainty, whether these discrepancies stem from inaccuracies in the original text or from limitations within the recognition system itself.

<figure>
  <img src="{{ '/assets/images/positerror.png' | relative_url }}" alt="Screenshot of Zoom Meeting">
</figure>

*a bug in PositCloud that we were able to fix thanks to Professor*

A factor that clearly affected the process of geocoding, and translating the textual data into mapped locations in PositCloud, was ensuring that each location was accurate in relation to the context of the text, as well as manually adding locations when they were not present. This is something that requires a level of human interpretation that an automated system could not fully replicate. For example, if I were to ask ChatGPT to generate code, it would produce a functional output; however, without precise instructions and contextual grounding, it would not necessarily yield the desired results. Similarly, in geocoding human input is essential to verify the accuracy of the data data as there is always a possibility of error when relying solely on automated systems. 

<iframe src="https://vyybui.github.io/hostedmaps/index.html" width="100%" height="500"></iframe> 

### Reflecting on the map
Once we were able to upload the HTML file to our repository and view the map through our GitHub website, it captured our attention how the data was visualized. Both the blue and orange points represent the Hadhramout places visited by the Bents, yet the automated and manual methods reveal both similarities and differences.

There is definitely a pattern between the manually (orange) and automatically (blue) geocoded locations. In both layers of the map, there is a cluster of dots around Africa and in the Arabian peninsula. This intuitively makes a lot of sense, given the nature and context of the text we were looking at. We also noticed that there are significantly more blue dots, which initially led us to believe that automatic geocoding is more efficient. For starters, the manually geocoded locations are mostly distributed across Africa, a few areas of Asia, mainly in the Middle East, and some parts of Europe. It was also interesting to note that there were only three secondary locations found in the Americas, all located within the United States. On other hand, the blue dots appear across a much wider range on the map. These locations span Africa, Europe, Asia, Australia, North America, South America, and even one location in Central America. This highlights the extensive scope of the Bents couple’s travels, which is confirmed by our initial research about the text. There are also various locations where dots overlap, which means that the latitude and longitude data is the same for both methods. This enhances the reliability of the geocoded location. 

The process of working with the Bent couple’s Chronicles through tools such as Recogito, GeoNames, and PositCloud revealed both the possibilities and limitations of digital mapping when applied to historical texts. While these systems allowed for the identification and visualization of a significant number of locations, they also exposed gaps in recognition, especially when dealing with outdated, inconsistent, or regionally specific place names. This made it evident that, although digital tools can facilitate the organization of and representation of spatial data, they cannot fully replace the interpretive role of a researcher.

There are also standalone orange dots and standalone blue dots. However, I noticed that, for example, in East Africa or Western Asia, these standalone dots would often have other dots, in the opposite color, somewhere around. This makes the exact location a bit ambiguous, but we also, at least, know that this region is mentioned in the original text.
I noticed that the Bents Hadhramout Places layer (automatic) identifies more locations in the Americas, Europe, and India. When I try to make sense of why that is, I reflect on my process of manual geocoding. I was definitely more “drawn” to the places around the Arabian peninsula, since these seem more relevant and important to the context. This might perhaps explain why I overlooked some of the Western locations, whereas with automatic geocoding, it treats every place with equal importance. I also suppose that automatic geocoding can easily identify locations in the West because of how prevalent they are, whereas I might accidentally skip over these names because I did not realize they were referring to places.

Looking at the map that we produced, I was really interested in the case of Türkiye and India.
- In Türkiye, there is one single blue dot (automatic) in the middle of the country; this suggests that automatic geocoding only picks up the country. Meanwhile, the orange dot (manual) points to the Turkish city Eskişehir.
- The opposite situation happens in India. A single orange dot identifies India as a country, but multiple blue dots are scattered across the cities of New Delhi, Mumbai, Bengaluru, etc.

I think that the representation of this can drastically change how we view the original text. Generally, I think that being more specific is better, and in this case, I think it also signifies the importance and relevance of the country in the context of the text Bents Hadhramout.

Connecting to the state name situation in “1, the Road,” I also realized a similar situation happened when we were doing manual geocoding in Recogito. The location “Mecca” was mentioned, and while it seems to refer to the holiest city in Islam, located in Saudi Arabia's Sirat Mountains, it was more known with the spelling Makkah. Meanwhile, there is an unincorporated community in California (USA), called “Mecca.” When we were doing the geocoding, an error occurred, and we accidentally pinpointed the wrong location.

In the original text, there were also mentions such as “near a little village called Tahiya,” “near Aden,” “near Shabwa,” etc. It was extremely difficult to pinpoint the exact location, so the closest thing we could do was tagging the location it was near to, in this case, Tahiya, Aden, and Shabwa. My rationale for doing this was if I can’t pinpoint the exact location, then pinpointing the region would be the next best thing. Because if I decided not to tag them at all, that is essentially making them invisible in the map.

Despite the supposition that the cultural and linguistic variation of a location’s name might affect whether the system recognizes it or not, the answer is more intricate than what it appears to be. Places like Makalla (regarded as “Al Mukalla” by the system), Hadhramout, Jehannam (which had to be flagged since it was displayed as “unknown”),  Akaba, and Wadi Adim (suggested to be “Lahij”), had slightly more complexity to their names, resulting in a more difficult process of identification by Recogito. Meanwhile other places like Medina, Basra, and Somali composed of “simpler words” were easily recognizable. Most of these names share similarities in respect to their origin, for example, “Wadi Adim” is an Arabic term originating from the phrase wada, meaning "it flowed, whereas “Basra” gets its name from the Arabic word "baṣrah," meaning "the over-watching," "the observer," or "the seeing. This highlights the complexity of whether the  cultural and linguistic variation factors on the recognition of a location, since two places of similar origins can produce different results. Thus, we believe that there is no definite answer as to what makes a location’s name more recognizable than the other, and that it all depends on the sophistication of the system itself.

### Work Cited

(1) The Arabian and Persian explorations, [http://tambent.com/the-arabian-and-persian-explorations/](http://tambent.com/the-arabian-and-persian-explorations/)


(2) Recogito, [https://recogito.pelagios.org/](http://tambent.com/the-arabian-and-persian-explorations/)

## READY FOR GRADING
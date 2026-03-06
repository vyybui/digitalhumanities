---
title: "Assignment 1: Working with a Corpus"
excerpt_separator: "<!--more-->"
categories:
  - Assignment
tags:
  - assignment
  - voyant
  - r
  - corpora
---

## Corpus Selection

For my corpus, I have decided to explore the [Art collection](https://gutenberg.org/ebooks/bookshelf/675) in [Project Gutenberg](https://gutenberg.org/). I chose to work with this topic because not only do I have a personal interest in art, but I was also curious to see **what kind of information do books in public databases have about something that relies heavily on visuals as art** (I don't often read art books, I usually prefer seeing them in person in galleries and museums). It will be especially cool if I learn something I had not known before (since placards at musuems only offer very little insights about the artworks themselves and the artists).
The texts I've chosen are:
* What Is Art? by graf Leo Tolstoy (64908)
* Lives of the Most Eminent Painters Sculptors and Architects, Vol. 01 (of 10) (25326)
* A History of Art for Beginners and Students: Painting, Sculpture, Architecture (24726)
* The Practice and Science of Drawing by Harold Speed (14264)
* The Venetian School of Painting by Evelyn March Phillipps (30098)

### Process & Rationale
When I was curating this corpus, I tried to choose texts that were **similar in length**. This is because if a text is significantly longer/shorter than the others, it will be over/underrepresented which **skews the data**. In the end, the five chosen texts are similar in length, with the longest text having 92349 words compared to the shortest text with 80030 words.
Although these books are all about Art, I wanted to choose books that were **written around the same time** to minimize the **extraneous variables** that might impact data. Most of the books in the corpus were written from mid-19th century to the early 20th century, with the exception of the book coded 25326 (written in the 1500s). While I understand that it can be an "outlier" or so, I decided to include it in the corpus to see if there are any visible differences when conducting distant reading.

I hypothesis that there will be a mix of 'art history' content and 'the practice of art' content. What I really mean by this is, some books will perhaps focus more on the historical contexts and the painters, such as books 25326 and 30098. Meanwhile, books like 64908 and 14264 are more likely to cover the technical aspect of art (for example: how to draw and paint, the building blocks of a painting, etc.). When I was researching these texts, I also noticed that most of these texts had something to do with Europe (whether that is about European art, or written by European authors, or both!). This naturally makes sense because given the context these books were written, art was mostly flourishing in Europe.

## Analysis
My corpus selection covers a wide-range of topics in Art, so it was definitely going to be interesting conducting distant reading. As instructed, I used Voyant Tools and RMarkdown on Posit Cloud, both of which are tools we have used in class, to do the distant reading. As I was playing around with the tools, I've taken notes of interesting details below.
### Visualizations
I personally am a visual learner so I found tools like Voyant Tools and the visualizations created in the RMarkdown to be extremely helpful. In this process of distant-reading, I'm trying to expand my understanding of art through **identifying patterns and recognizing interesting key terms**. Most of the time, this means identifying a common theme throughout the corpus, such as religion and history. These are the things that can be represented visually through paintings, but I also wanted to see how they are recorded in these books. Hence, I used a variety of tools to 'look up' terms, such as the heat map and the trend graph, as well as tools that spot patterns, such as the TeamBerry visualization. I also included 2 distinct word clouds made in each of the tool and study them carefully.
#### RMarkdown
I really enjoy the **color-coded word cloud** feature in RMarkdown. It allows me to see which group of words belongs to which text (through the legend), which gives me a better idea of which aspect of art they are talking about. They also help me confirm (or reject) my initial hypothesis about the content of these books. However, a potential set back might be that this word cloud **does not distinguish words** that appear in 2 or more books, which can potentially mislead my interpretation of the corpus.

<figure>
  <img src="{{ '/assets/images/a1ccwc.png' | relative_url }}" alt="Word cloud">
</figure>

*My color-coded word cloud for my corpus (5 texts)*
I referenced [The Elements and Principles of Art](https://massart.edu/app/uploads/legacy-files/Principles%20and%20Elements.pdf) and tried to form a connection between technical art terms. For example, *line, light, dark, illustration* all appear in Harold Speed's *The Practice and Science of Drawing*. Although this may not explicitly reveal what the book is about, we can kind of sense that it covers more of the practice of art compared to book *24726* which includes terms like *church, impression, death, unity, meaning*. 
What I learned in this process too, is to play around with the code! I was experiencing issues with the legend being too big and covering almost all of the word cloud, but then I did a bit of research and learned some parameters I could add to shrink the legend.

This is the **Scaled Frequency Heat Map**. The words I've chosen are all Italian-related. I was curious to see how often (or not) Italy was mentioned in the corpus. Before my actually running the code, I hypothesized that the book *The Venetian School of Painting by Evelyn March Phillipps (30098)* will allude to Italy the most, for obvious reasons. Initally, I was worry that this specific text would skew the dataset because of the specificity of the geographical location, but the results of the frequency heat map completely surprised me!

The words I've chosen are: *Rome*, *Florence*, *Venice* (primary Italian cities associated with artistic developments (partially due to the Silk Road trading)), *Titian* (a very famous Italian painter), and *Italy*. The photo below shows the map.

<figure>
  <img src="{{ '/assets/images/a1heatmap.png' | relative_url }}" alt="Scaled Frequency Heat Map">
</figure>

*My Scaled Frequency Heat Map for Italy-related terms*

I did not expect to see Italy being referenced in books other than *30098*. However, what surprised me even more is that Rome, Florence, and Venice appeared a lot, but in 3 completely different books.  Meanwhile, there is a correlation between the mention of Venice and Titian in book *30098*, which led me to **suspect that Titian is from Venice. A Google search confirms that Titian was born in a different Italian city, but lived and worked in Venice for the vast majority of his life**. This was a detail I did not know before!

#### Voyant Tools
Something that Voyant Tools allows me to do (easily) is to **add additional stopwords** (whereas I was not able to figure out how to do so in R). My texts are all from Project Gutenberg, so I wanted to remove any irrelevant watermarks out of the dataset. Specificaly, the words I have added to the default stopword list on Voyant Tools are: *Project; Gutenberg; sec; footnote; eBook; chapter*. Although the effect can be minimal because my corpus size is small (5 items), having a different stop-word list can result in Voyant Tools and RMarkdown giving me different data visualizations (Wordclouds, for example). In fact, this was mentioned in by **Rockwell and Sinclair in [*The Measured Words: How Computers Analyze Text*](https://doi.org/10.7551/mitpress/9522.003.0003)**, in which they suggest that having different stop-word lists can result in different data representation (page 35 and Figure 2.7 in page 29).

**TermBery iFrame**

 I decided to include this TermBerry visualization as an iFrame because I thought that it would be interesting to see the **collocate frequencies** (by default two words the left and two words to the right) for the words. Including it as an iFrame allows me to hover the words and explore their relationships. For example, hovering on *'art'* highlights *'work'* and *'works'* potentially because "works of art" and "work of art" are popular terms (this is my prediction). For me, hovering and playing with the iFrame **naturally encourages my brain to explain certain connections (literally coming up with an answer to why some words are related when they seem very disconnected)**, as well as prompt questions about the context in which certain words/phrases were used. I think that is is a very 'normal' aspect of distant reading, though, since what I'm looking at is essentially patterns rather than details. This tendency to intepret data is also mentioned by Rockwell and Sinclair about word clouds (although I think it can apply beyond word clouds as well) as "different affordances for interpretation." (page 35)

<iframe style='width: 418px; height: 322px;' src='https://voyant-tools.org/tool/TermsBerry/?stopList=keywords-36e7d961f0c3de433d22b3bb854924da&corpus=5b0f5687b3374202f5ab53af19474e4d'></iframe>

I think that this is a really cool feature and I was asking myself how could something like this be implemented in real life. Then, I suddenly remember a video I watched a couple months ago about **machine learning, particularly Large Language Models (LLM)**. These LLMs are fed previous data and the way it works is that it predicts what the next word is based on this fed data combined with an algorithm that involves weight and bias. 

**Other Tools**

Unlike the previous word cloud made with RMarkdown, this Voyant word cloud is not color-coded, and the words shown are based on their popularity across all 5 items in the corpus. The reason why I chose to create another word cloud is because I wanted to **compare and contrast** them and determine which one is "better" for distant reading.

<figure>
  <img src="{{ '/assets/images/a1vcloud.png' | relative_url }}" alt="Trend Graph for Religion-related words">
</figure>

I definitely do see some similarities between the 2 word clouds, in other words, words that appear in both 'clouds.' *Art, painting, painted, drawing, life, church, madonna*, are only some of the many words that the words clouds shares. I think that the preference for which type of word cloud depends entirely on the purpose of the research, but as of now, I do find the RMarkdown color-coded cloud to be somewhat more informative as it **specifies the origin** of the words.

Besides Italian-related terms, I also noticed a number of religion-related words. In order to see the relationship between each book and religion, I used a *trend graph* to map out the relative frequencies of words such as: *chapel, religious, church, christ, saint*.
<figure>
  <img src="{{ '/assets/images/a1trend.png' | relative_url }}" alt="Trend Graph for Religion-related words">
</figure>

*Trend Graph for Religion-related Terms*

The relative frequency of each word, calculated by the number of times a word appears divided by the total number of words in the text, shows how 'dense' it appears throughout the text. From the graph, we can see that all texts, except for one (book *14264*), have *some* mention of religion. From the title of book *14264* -- *The Practice and Science of Drawing* by Harold Speed -- perhaps this book focuses on the technical aspect of drawing, rather than the cultural context around it. "Church" is mentioned significantly more in book *25323* and so is "Saint" in *30098*. From this graph, we can see that there is a potential relationship between art history and the Church, since it probably is not a coincident that 4/5 of the books I've chosen has some form of religious terms.

## Reflection

I have covered a substantial amount of reflection questions above, but there are still some things that I would like to highlight!

On **computational insights**, I think that distant-reading has allowed me to briefly scratch through the surface of art history in a very short amount of time. I learned things that I did not know before, and in an interesting way as well (making hypotheses and confirming them, for example), which makes the learning process a bit more "memorable." That said though, the amount of information I learned from merely viewing these visualizations is not a lot. Of course, linear reading would actually teach me a lot more, and by the end of the linear reading, I would know much much more about art practices and art history. My corpus is small since it only has 5 texts, so if I were to read them all, it would take quite some time. On the broader context, it would be impossible to read all texts in a large corpus and this is where distant reading comes in to play. I also appreciate that doing this process computationally allows me to only focus on the keywords, instead of having to read 19/20th century literature, which can be a more difficult task.

However, I also want to highlight a quote by Adwetewa-Badu from the [High Theory podcast](https://newbooksnetwork.com/distant-reading) that I think is really accurate: "One cannot do distant reading without also, at some point, having to do very close, attentive reading." (06:55). The author suggests that it is rather a "hand-in-hand" process, and I can relate to this a lot. In order to make sense of the visualizations and make sense of the data we get from distant-reading, we have to also look closely at the original texts.

With my small corpus, it is easier to "cherry-pick" 5 texts to study. When I say "cherry-pick," I mean the fact that they were carefully considered in terms of publication date, language, geographical region, and text length. If I were to build a larger corpus, it will be a lot more difficult to ensure all items within the corpus are similar and ideal for distant-reading. However, having only 5 texts can of course, under-represent the huge scope of Art. This corpus is basically a sample of 5 books (that were NOT randomly chosen) and so it would be difficult for me to generalize the findings from my distant-reading to the topic of Art, simply because it lacks many details and does not do a good job of accurately represent the topic. If I were to do this will all of the books under the Art collection in Project Gutenberg though, I would potentially have had a 'better' result (not saying that it represents ALL of art--just definitely closer to my current corpus that has 5 items). So for a small-scale project like this assignment, I think that it is appropriate to start out will a small corpus. What this does is it simply "scratches the surface" of this topic. Right now, it is very much managable, but if I were to do research by conducting distant-reading, 5 texts is definitely not enough for a topic that has a lot of breadth and depth like art. Having a bigger corpus would make more sense in terms of representation and generalizability, but obviously it would be a lot more difficult to handle.

Distant-reading, with tools like the RMarkdown and Voyant Tools, can be really powerful to study previous research and related books/materials. However, I will also keep in mind what using these tools mean for my data collection. As [Underwood](https://newbooksnetwork.com/distant-reading) suggests, "scholars cannot adopt a new mode of interpretation without fully understanding the reasoning it implies." I think that is this a very powerful reminder to use data collection tools responsibly, meaning awareness of the limitations (and potential biases!) of the tools. That said, I do see distant-reading as an effective and interesting way of conducting research. I'm definitely going to have to do research, whether that is the university's, my Capstone, or my future personal projects.

This Assignment 1 has been a great introduction to distant-reading, Voyant Tools, and RMarkdown. I genuinely enjoyed exploring and doing this assignment, because although I am interested in Art, I have probably never interact with these kind of books and have also never did distant-reading. So, there was a lot of fun learning, and it's definitely things that I can bring with me beyond the scope of this course!

## READY FOR GRADING
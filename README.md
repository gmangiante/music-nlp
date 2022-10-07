### GenreBot : Using Natural Language Processing in Music Marketing

**BACKGROUND**

As a Spotify cross-genre marketing analyst, it's my job to stay on top of the content that's trending on the music scene, and to employ my knowledge to provide the best, most relevant content to Spotify listeners in their high-affinity genres. One of the ways I learn about what's hot right now is by scanning aggregated social media feeds from a variety of sources, using tools such as [Sprout](https://sproutsocial.com).

However, I'm finding that the amount of content I need to survey is prohibitively large, and is not broken down in a way that corresponds to my genre markets. I need a better, automated way to ingest social media text content in a platform-agnostic way, tag it to the most relevant genre, and extract the top trending content. In addition to informing my marketing campaigns, this information can be passed on to my colleagues developing and maintaining our recommendation engine, enhancing the relevance of their results.

**PROPOSED SOLUTION**

I know that there is a [PushShift API](https://github.com/pushshift/api) that will allow me to download Reddit posts, tagged to their respective subreddits. I want to use this Reddit data as the training material for GenreBot, my new genre identification and content extraction engine. For my first foray into Natural Language Processing (NLP), I will:
- use the PushShift API to download posts from 2 (or more) music-related subreddits
- clean that data using regular expressions and other text manipulation utilities
- explore the content of that data to better understand it
- employ a broad spectrum of NLP tools and machine learning to train the most accurate model I can
- use my production model to predict the genre for each new post I receive, and incorporate the text from the post into my genre-tagged corpus so that I can extract updated trending words and phrases

**WHAT SUCCESS LOOKS LIKE**
By the end of this machine learning project, I want to arrive at a model that will accurately predict the relevant genre of a given post at a rate of 80% or above, selecting from 2 possible subreddits. I then want to be able to extract the top 10 trending words and phrases from the updated corpus for each genre to use in our marketing and recommendation efforts.
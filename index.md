# SPOTIFY PODCAST DATASET
	Podcasts are a rapidly growing audio-only medium that involve new patterns of usage and new communicative conventions and motivate research in many new directions.To facilitate such research, we present the Spotify English-Language Podcast Dataset. 
	This dataset consists of 100,000 episodes from different podcast shows on Spotify. The dataset is available for research purposes.

The dataset was initially created for use in the the TREC Podcasts Track shared tasks. Participants were asked to work on two tasks focusing on understanding podcast content, and enhancing the search functionality within podcasts. 

We are releasing this dataset more widely to facilitate research on podcasts through the lens of speech and audio technology, natural language processing, information retrieval, and linguistics. The dataset contains about 50,000 hours of audio, and over 600 million transcribed words. The episodes span a variety of lengths, topics, styles, and qualities.

The podcast dataset contains about 100k podcasts filtered to contain only documents which the creator tags as being in the English
 language, as well as by a language filter applied to the creator-provided title and description. We expect that there will be
 a small amount of multilingual content that may have slipped through
 these filters.


<p>Episodes were sampled from both professional and amateur podcasts including:
<ul><li>
	Episodes produced in a studio with dedicated equipment by trained professionals</li>
<li>
Episodes self-published from a phone app - these vary in quality depending on professionalism and equipment of the creator.
</li>
	</ul>
<div>
	<p>
The episodes represent a wide range of:
</p>

	<ul><li>
Audio quality: we can expect professionally produced podcasts to have high audio quality, but there is significant variability in the amateur podcasts. We have included a basic popularity filter to remove most podcasts that are defective or noisy.<\/li><li>Topics: the episodes represent a wide range of topics, both coarse- and fine-grained. These include lifestyle and culture, storytelling, sports and recreation, news, health, documentary, and commentary.<\/li><li>Formats: podcasts are structured in a number of different ways. These include scripted and unscripted monologues, interviews, conversations, debate, and included clips of other non-speech audio material.
</li></ul>
    <p>
</div>

    <div class="header">
      CONTENTS OF THE DATASET
    </div>
    <div>
      <p>
	Each of the 100,000 episodes in the dataset includes an audio file, a text transcript, and some associated metadata.
      </p>
      <p>
	Note that the data does <strong>not</strong> include listening data or other user or usage-related data.
      </p>
    </div>
    <div class="header">Audio data</div>
    <div class="brodtext">
      <p>
       Files in OGG format
      </p>
      <p>
	Median duration of an episode ~ 31.6 minutes
      </p>
      <p>
	Estimated size: ~2 TB for entire audio data set
      </p>
    </div>
    <div class="header">
      Metadata
    </div>
    <div class="brodtext">
      <p>
	Extracted basic metadata file in TSV format with fields:<em>show_uri, show_name, show_description, publisher, language, rss_link, episode_uri, episode_name, episode_description, duration</em>
      </p>
    </div>
    <div class="header">Episode RSS header files</div>
    <div class="brodtext">
      <p>
	~1000 words with additional fields of potential interest, not necessarily aligned for every episode: channel, title, description, author, link, copyright, language, image
      </p>
      <p>
	Estimated size: 145MB total for entire RSS set when compressed.
      </p>
    </div>
    <div class="header">
      Transcripts
    </div>
    <div class="brodtext">
      <p>
	JSON format
      </p>
      <p>
	Average length is just under 6000 words, ranging from a small number of extremely short episodes to up to 45,000 words. Two-thirds of the transcripts are between about 1,000 and about 10,000 words in length; about 1% or 1,000 episodes are very short trailers to advertise other content.
      </p>
      <p>
	Estimated size: 12GB for entire transcript set.
      </p>
    </div>
    <div class="header">
      Audio features
    </div>
    <div class="brodtext">
      <p>
	OpenSmile audio features
      </p>
      <p>
	eGeMAPS low level acoustic descriptors and functionals computed for overlapping 1.01s windows (75GB) saved in HDF5 format. 
      </p>
      <p>
	Yamnet audioevents
      </p>
      <p>
	1024-dimensional embedding vectors for overlapping 0.96s segments for the podcasts (400GB) and Yamnet event class scores (60GB), saved in HDF5 format. 
      </p>
    </div>
<!-- ","website":null,"font":null,"source":"admin","sort_order":"0","start_date":null,"start_time":null,"end_time":null,"tweet_id":"","created":"2020-11-30 12:26:54","parent_splash_feed_id":null,"title":"","subtitle":"","image_url":"","temp_row":"0","raw_body":"0","options":[],"embed_code":null,"deleted":"0"}},{"element":"custom-block-3033944218","name":"Text","block_type":"content","gid":515545935,"superType":"","SplashFeed":{"id":"3033944218","event_id":"457702655","user_id":null,"foreign_event_id":null,"type":"content","body":"<p><strong>Example of Transcript:</strong>
</p>
<p>
<br>
The transcripts consist of a JSON structure. The below figure demonstrates the \"results\" structure which begins with a list of transcriptions of 30 second chunks of speech, each such chunk with a confidence score and with every word annotated with \"startTime\" and \"endTime\". The last item in the \"results\" structure is a list of all words for the entire episode, again with with \"startTime\" and \"endTime\" and in addition an inferred \"speakerTag\" to distinguish episode participants. While the \"results\" structure is designed to accommodate several hypotheses through its \"alternatives\" list structure, this present transcription does not provide alternative transcription hypotheses.
</p>
<p>
</p>
<p>
</p>
<p> <tt>{\"results\":</tt>
</p>
<p><tt>[{\"alternatives\": // always only one alternative in these transcripts</tt>
</p>
<p><tt>[{\"transcript\": \"Hello, y'all, ... &lt;30 s worth of text&gt; ... \",</tt>
</p>
<p><tt>\"confidence\": 0.8640950322151184,</tt>
</p>
<p><tt>\"words\": // list of words</tt>
</p>
<p><tt>[{\"startTime\": \"3s\", \"endTime\": \"3.300s\", \"word\": \"Hello,\"},</tt>
</p>
<p><tt>...</tt>
</p>
<p><tt>]}]},</tt>
</p>
<p><tt>{\"alternatives\": [</tt>
</p>
<p><tt>{\"transcript\": \"Aaron ... \",</tt>
</p>
<p><tt>\"confidence\": 0.7733442187309265,</tt>
</p>
<p><tt>\"words\": [</tt>
</p>
<p><tt> {\"startTime\": \"30s\", \"endTime\": \"30.200s\", \"word\": \"Aaron\"}, ... ]}]},</tt>
</p>
<p><tt>{\"alternatives\": // last item in \"results\": a straight list of words with \"speakerTag\"</tt>
</p>
<p><tt>[{\"words\":</tt>
</p>
<p><tt>[{\"startTime\": \"3s\", \"endTime\": \"3.300s\", \"word\": \"Hello,\", \"speakerTag\": 1},</tt>
</p>
<p><tt>...</tt>
</p>
<p><tt>{\"startTime\": \"30s\", \"endTime\": \"30.200s\", \"word\": \"Aaron\", \"speakerTag\": 1},</tt>
</p>
<p><tt>...</tt>
</p>
<p><tt></tt>
</p>
<p><tt>{\"startTime\": \"39.900s\", \"endTime\": \"40.500s\", \"word\": \"salon.\", \"speakerTag\": 2} ] }] }]</tt>
</p>
<p><tt>}</tt>
</p>
<p>
</p>
","website":null,"font":null,"source":"admin","sort_order":"0","start_date":null,"start_time":null,"end_time":null,"tweet_id":"","created":"2020-11-30 12:26:54","parent_splash_feed_id":null,"title":"","subtitle":"","image_url":"","temp_row":"0","raw_body":"0","options":[],"embed_code":null,"deleted":"0"}},{"element":"custom-block-3033944224","name":"Text","block_type":"content","gid":243635221,"superType":"","SplashFeed":{"id":"3033944224","event_id":"457702655","user_id":null,"foreign_event_id":null,"type":"content","body":"<p><strong>
<br>
</strong>
</p>
<p><strong></strong>
</p>
","website":null,"font":null,"source":"admin","sort_order":"0","start_date":null,"start_time":null,"end_time":null,"tweet_id":"","created":"2020-11-30 12:26:54","parent_splash_feed_id":null,"title":"","subtitle":"","image_url":"","temp_row":"0","raw_body":"0","options":[],"embed_code":null,"deleted":"0"}}]}]}]}]},{"class":"container-ele element","contain":"1","dope-section":1,"name":"Date Block","gid":745258300,"type":"simple-container","superType":"container","options":{"matchHeight":[]},"layout_block_id":"59602","group":[{"class":"container-ele element","contain":"1","name":"Content Container","gid":447195272,"type":"simple-container","superType":"container","options":{"matchHeight":[]},"group":[{"name":"Headline Container","gid":905326267,"type":"simple-container","superType":"container","options":{"matchHeight":[]},"group":[{"name":"Column One","gid":811809820,"type":"simple-container","superType":"container","options":{"matchHeight":[]},"group":[{"block_type":"headline","element":"custom-block-3033926117","inherited-theme":"","gid":606275523,"superType":"","SplashFeed":{"id":"3033926117","event_id":"457702655","user_id":null,"foreign_event_id":null,"type":"headline","body":"","website":null,"font":null,"source":"admin","sort_order":"0","start_date":null,"start_time":null,"end_time":null,"tweet_id":"","created":"2020-11-30 11:58:03","parent_splash_feed_id":null,"title":"<p>Editors
<br>
-->


<p>
    Ann Clifton, Joana Coreia, Md Iftekhar Tanveer, Jussi Karlgren, Ben Carterette, Rosie Jones
</p>

<!--
","website":null,"font":null,"source":"admin","sort_order":"0","start_date":null,"start_time":null,"end_time":null,"tweet_id":"","created":"2020-11-30 11:58:03","parent_splash_feed_id":null,"title":"","subtitle":"","image_url":"","temp_row":"0","raw_body":"0","options":[],"embed_code":null,"deleted":"0"}}]}]}]}]},{"class":"container-ele element","contain":"1","dope-section":1,"name":"Date Block","gid":527383149,"type":"simple-container","superType":"container","options":{"matchHeight":[]},"layout_block_id":"59602","group":[{"class":"container-ele element","contain":"1","name":"Content Container","gid":750152004,"type":"simple-container","superType":"container","options":{"matchHeight":[]},"group":[{"name":"Headline Container","gid":187910755,"type":"simple-container","superType":"container","options":{"matchHeight":[]},"group":[{"name":"Column One","gid":218244185,"type":"simple-container","superType":"container","options":{"matchHeight":[]},"group":[{"block_type":"headline","element":"custom-block-3033911158","inherited-theme":"","gid":73931467,"superType":"","SplashFeed":{"id":"3033911158","event_id":"457702655","user_id":null,"foreign_event_id":null,"type":"headline","body":"","website":null,"font":null,"source":"admin","sort_order":"0","start_date":null,"start_time":null,"end_time":null,"tweet_id":"","created":"2020-11-30 11:28:15","parent_splash_feed_id":null,"title":"<p>FAQ
<br>

</p>
","subtitle":"","image_url":"","temp_row":"0","raw_body":"0","options":[],"embed_code":null,"deleted":"0"}}]},{"name":"Column Two","gid":468807503,"type":"simple-container","superType":"container","options":{"matchHeight":[]},"group":[{"element":"custom-block-3033911157","name":"Text","block_type":"content","gid":706636771,"superType":"","SplashFeed":{"id":"3033911157","event_id":"457702655","user_id":null,"foreign_event_id":null,"type":"content","body":"
-->

<!--
 <p><strong>Is the dataset multilingual?</strong>
<br>

</p>
<p>
<br>
Episodes are limited to English as the primary language, but we hope to release successive multilingual versions of the dataset in the future.
</p>
<p>All information included in this dataset is pulled from content that is already publicly available on Spotify\u2019s service (i.e. metadata and content of published podcast episodes)
</p>
<p>
<br>

</p>
<p><strong>Does the dataset contain user behavior?</strong>
</p>
<p>
<br>

</p>
<p>The dataset does not contain any user behavior information.
</p>
-->



<!--
<p><strong>What were the TREC Podcasts Track Tasks?</strong>
</p>
<p>
<br>

</p>
<p>We defined two tasks for participants in the TREC Podcasts Track.
</p>
<p>
<br>

</p>
<p><strong>Task 1: Ad-hoc Segment Retrieval</strong>
</p>
<p>
<br>
Given an arbitrary keyword query, retrieve the jump-in point for relevant segments of podcast episodes. The best result would be a segment with very relevant content, which is also a good jump-in point for the user to start listening. We added some non-topical ranking criteria for the 2021 edition.
</p>
<p>
<br>

</p>
<p>and
</p>
<p>
</p>
<p>
</p>
<p><strong>Task 2: Summarization</strong>
</p>
<p>
</p>
<p>
</p>
<p>Given a podcast episode with its audio and transcription, return a short snippet capturing the most important information in the content. 
</p>
<p>
<br>

</p>
<p>   <span style=\"text-decoration:underline;color:#0ae889;\"><a class=\"fontColorEdited\" style=\"color:#0ae889;text-decoration:underline;\" href=\"https://trecpodcasts.github.io/\">More information about the TREC Podcasts Track</a></span>
</p>
<p>
<br>

</p>
<p>
<br>

</p>
<p><strong>What if there are inaccuracies in the data?</strong>
<br>

</p>
<p>
<br>
All RSS headers and audio are supplied by creators, and Spotify does not claim responsibility for the content therein. All transcripts are generated using automatic speech recognition, and may contain errors; Spotify makes no claim that these are accurate reproductions of the audio content.
</p>
<p>
<br>
<strong>Who should be excited by this dataset?</strong>
</p>
<p>
<br>

</p>
<p>Speech, NLP and Information Retrieval researchers who want to develop novel models on previously inaccessible streams of data. Also, any researchers interested in podcasts!
<br>

</p>
<p><strong>Who runsthe TREC shared task?</strong>
</p>
<p>
<br>

</p>
<p>The competition was a collaboration between Spotify, NIST (the National Institute of Standards and Technology), CLARIN, Dublin City University, and TREC (the Text Retrieval Conference). Spotify supplies the data, the annotation standards, and the evaluation metrics. TREC supplies the infrastructure for participants to join the competition, submit their entries, and publish their system descriptions, and organizes a conference in November where participants share their results. NIST supplies the expert human annotators who will judge the participants\u2019 entries according to Spotify\u2019s annotation guidelines and metrics.
</p>
<p>
<br>
<strong>What are some helpful resources we can look at if we want to learn more?</strong>
</p>
<p>
<br>

</p>
<p>The previous Spoken Document Retrieval task at TREC: <a class=\"custom-button\" href=\"https://pdfs.semanticscholar.org/57ee/3a15088f2db36e07e3972e5dd9598b5284af.pdf\">https://pdfs.semanticscholar.org/57ee/3a15088f2db36e07e3972e5dd9598b5284af.pdf</a>
</p>
<p>
<br>

</p>
<p><strong>Who can I reach out to if I have a question?
<br>

<br>
</strong>
</p>
<p>Contact the organizers: podcasts-challenge-organizers@spotify.com
</p>
<p>
</p>
<p>
<br>

</p>
<p>
<br>

</p>
","website":null,"font":null,"source":"admin","sort_order":"0","start_date":null,"start_time":null,"end_time":null,"tweet_id":"","created":"2020-11-30 11:28:15","parent_splash_feed_id":null,"title":"","subtitle":"","image_url":"","temp_row":"0","raw_body":"0","options":[],"embed_code":null,"deleted":"0"}}]}]}]}]},{"class":"container-ele element","contain":"1","dope-section":1,"name":"Date Block","gid":698899738,"type":"simple-container","superType":"container","options":{"matchHeight":[]},"layout_block_id":"59602","group":[{"class":"container-ele element","contain":"1","name":"Content Container","gid":215500541,"type":"simple-container","superType":"container","options":{"matchHeight":[]},"group":[{"name":"Headline Container","gid":488691327,"type":"simple-container","superType":"container","options":{"matchHeight":[]},"group":[{"name":"Column One","gid":848592469,"type":"simple-container","superType":"container","options":{"matchHeight":[]},"group":[{"block_type":"headline","element":"custom-block-3040244988","inherited-theme":"","gid":653265597,"superType":"","SplashFeed":{"id":"3040244988","event_id":"457702655","user_id":null,"foreign_event_id":null,"type":"headline","body":"","website":null,"font":null,"source":"admin","sort_order":"0","start_date":null,"start_time":null,"end_time":null,"tweet_id":"","created":"2020-12-23 11:03:14","parent_splash_feed_id":null,"title":"<p>Citing the dataset
<br>

</p>
","subtitle":"","image_url":"","temp_row":"0","raw_body":"0","options":[],"embed_code":null,"deleted":"0"}}]},{"name":"Column Two","gid":909413765,"type":"simple-container","superType":"container","options":{"matchHeight":[]},"group":[{"element":"custom-block-3040244989","name":"Text","block_type":"content","gid":640379897,"superType":"","SplashFeed":{"id":"3040244989","event_id":"457702655","user_id":null,"foreign_event_id":null,"type":"content","body":"<p><strong></strong>
</p>
<p>When referring to the data, please cite the following paper: 
</p>
<p>
<br>

</p>
<p>\u201c100,000 Podcasts: A Spoken English Document Corpus\u201d by Ann Clifton, Sravana Reddy, Yongze Yu, Aasish Pappu, Rezvaneh Rezapour, Hamed Bonab, Maria Eskevich, Gareth Jones, Jussi Karlgren, Ben Carterette, and Rosie Jones, COLING 2020
</p>
<p>https://www.aclweb.org/anthology/2020.coling-main.519/
</p>
<p>
<br>

</p>
<p>Bibtex:
</p>
<p>
<br>
@inproceedings{clifton-etal- 2020-100000,
</p>
<p>title = \"100,000 Podcasts: A Spoken {E}nglish Document Corpus\",
</p>
<p>author = \"Clifton, Ann and
</p>
<p>Reddy, Sravana and
</p>
<p>Yu, Yongze and
</p>
<p>Pappu, Aasish and
</p>
<p>Rezapour, Rezvaneh and
</p>
<p>Bonab, Hamed and
</p>
<p>Eskevich, Maria and
</p>
<p>Jones, Gareth and
</p>
<p>Karlgren, Jussi and
</p>
<p>Carterette, Ben and
</p>
<p>Jones, Rosie\",
</p>
<p>booktitle = \"Proceedings of the 28th International Conference on Computational Linguistics\",
</p>
<p>month = dec,
</p>
<p>year = \"2020\",
</p>
<p>address = \"Barcelona, Spain (Online)\",
</p>
<p>publisher = \"International Committee on Computational Linguistics\",
</p>
<p>url = \"https://www.aclweb.org/ anthology/2020.coling-main.519 \",
</p>
<p>pages = \"5903--5917\",
</p>
<p>abstract = \"Podcasts are a large and growing repository of spoken audio. As an audio format, podcasts are more varied in style and production type than broadcast news, contain more genres than typically studied in video data, and are more varied in style and format than previous corpora of conversations. When transcribed with automatic speech recognition they represent a noisy but fascinating collection of documents which can be studied through the lens of natural language processing, information retrieval, and linguistics. Paired with the audio files, they are also a resource for speech processing and the study of paralinguistic, sociolinguistic, and acoustic aspects of the domain. We introduce the Spotify Podcast Dataset, a new corpus of 100,000 podcasts. We demonstrate the complexity of the domain with a case study of two tasks: (1) passage search and (2) summarization. This is orders of magnitude larger than previous speech corpora used for search and summarization. Our results show that the size and variability of this corpus opens up new avenues for research.\",
</p>
<p>}
</p>
<p>
</p>
<p>
</p>
<p>
<br>

</p>
<p>
<br>

</p>
","website":null,"font":null,"source":"admin","sort_order":"0","start_date":null,"start_time":null,"end_time":null,"tweet_id":"","created":"2020-12-23 11:03:14","parent_splash_feed_id":null,"title":"","subtitle":"","image_url":"","temp_row":"0","raw_body":"0","options":[],"embed_code":null,"deleted":"0"}}]}]}]}]},{"class":"container-ele element dope-section","contain":"1","dope-section":1,"name":"Text Block #1","gid":838072651,"type":"simple-container","superType":"container","options":{"matchHeight":[]},"group":[{"name":"Block Content","contain":"1","class":"","gid":844046559,"type":"simple-container","superType":"container","options":{"matchHeight":[]},"group":[{"block_type":"headline","element":"custom-block-3145856540","inherited-theme":"false","gid":43758635,"superType":"","SplashFeed":{"id":"3145856540","event_id":"457702655","user_id":null,"foreign_event_id":null,"type":"headline","body":"","website":null,"font":null,"source":"admin","sort_order":"0","start_date":null,"start_time":null,"end_time":null,"tweet_id":"","created":"2021-10-14 09:40:05","parent_splash_feed_id":null,"title":"<p>Published Research on the Spotify English Language Podcast Dataset
<br>

</p>
","subtitle":"","image_url":"","temp_row":"0","raw_body":"0","options":[],"embed_code":null,"deleted":"0"}},{"block_type":"content","element":"custom-block-3145856537","properties":[],"gid":898008175,"superType":"","SplashFeed":{"id":"3145856537","event_id":"457702655","user_id":null,"foreign_event_id":null,"type":"content","body":"<p>If you want your work included here, get in touch!
</p>
","website":null,"font":null,"source":"admin","sort_order":"0","start_date":null,"start_time":null,"end_time":null,"tweet_id":"","created":"2021-10-14 09:40:05","parent_splash_feed_id":null,"title":"","subtitle":"","image_url":"","temp_row":"0","raw_body":"0","options":{"modified":"0"},"embed_code":null,"deleted":"0"}},{"class":"container-2col container-ele element has-columns","contain":1,"name":"Container (2 col)","options":{"matchHeight":{"desktop":{"":"children"}}},"gid":175666336,"superType":"container","group":[{"class":"container-2col container-ele element has-columns","contain":1,"name":"Container (2 col)","options":{"matchHeight":{"desktop":{"":"children"}}},"gid":939159593,"superType":"container","group":[{"name":"Column 1","contain":1,"class":"","gid":126079079,"superType":"container","group":[{"element":"custom-block-3145856543","name":"Text","block_type":"content","gid":354588863,"superType":"","SplashFeed":{"id":"3145856543","event_id":"457702655","user_id":null,"foreign_event_id":null,"type":"content","body":"<p>TREC 2020
</p>
<p>
</p>
","website":null,"font":null,"source":"admin","sort_order":"0","start_date":null,"start_time":null,"end_time":null,"tweet_id":"","created":"2021-10-14 09:40:05","parent_splash_feed_id":null,"title":"","subtitle":"","image_url":"","temp_row":"0","raw_body":"0","options":[],"embed_code":null,"deleted":"0"}}],"type":"simple-container"},{"name":"Column 2","contain":1,"class":"","gid":623235025,"superType":"container","group":[{"element":"custom-block-3145856545","name":"Text","block_type":"content","gid":594293609,"superType":"","SplashFeed":{"id":"3145856545","event_id":"457702655","user_id":null,"foreign_event_id":null,"type":"content","body":"<p>Rosie Jones, Ben Carterette, Ann Clifton, Maria Eskevich, Gareth JF Jones, Jussi Karlgren, Aasish Pappu, Sravana Reddy, and Yongze Yu. \"TREC 2020 Podcasts Track Overview.\" In the Twenty-Ninth Text REtrieval Conference Proceedings (TREC 2020).NIST Special Publication 1266. Ellen M. Voorhees and Angela Ellis (editors). 2021.
</p>
<p>
</p>
","website":null,"font":null,"source":"admin","sort_order":"0","start_date":null,"start_time":null,"end_time":null,"tweet_id":"","created":"2021-10-14 09:40:05","parent_splash_feed_id":null,"title":"","subtitle":"","image_url":"","temp_row":"0","raw_body":"0","options":[],"embed_code":null,"deleted":"0"}},{"element":"custom-block-3145856541","name":"Text","block_type":"content","gid":780620339,"superType":"","SplashFeed":{"id":"3145856541","event_id":"457702655","user_id":null,"foreign_event_id":null,"type":"content","body":"<p>https://arxiv.org/abs/2103.15953
</p>
","website":null,"font":null,"source":"admin","sort_order":"0","start_date":null,"start_time":null,"end_time":null,"tweet_id":"","created":"2021-10-14 09:40:05","parent_splash_feed_id":null,"title":"","subtitle":"","image_url":"","temp_row":"0","raw_body":"0","options":[],"embed_code":null,"deleted":"0"}},{"element":"custom-block-3145856542","name":"Text","block_type":"content","gid":459548625,"superType":"","SplashFeed":{"id":"3145856542","event_id":"457702655","user_id":null,"foreign_event_id":null,"type":"content","body":"<p>https://trec.nist.gov/pubs/trec29/trec2020.html
</p>
","website":null,"font":null,"source":"admin","sort_order":"0","start_date":null,"start_time":null,"end_time":null,"tweet_id":"","created":"2021-10-14 09:40:05","parent_splash_feed_id":null,"title":"","subtitle":"","image_url":"","temp_row":"0","raw_body":"0","options":[],"embed_code":null,"deleted":"0"}}],"type":"simple-container"}],"type":"simple-container"},{"class":"container-2col container-ele element has-columns","contain":1,"name":"Container (2 col)","options":{"matchHeight":{"desktop":{"":"children"}}},"gid":291012331,"superType":"container","group":[{"name":"Column 1","contain":1,"class":"","gid":871574859,"superType":"container","group":[{"element":"custom-block-3145856539","name":"Text","block_type":"content","gid":142194392,"superType":"","SplashFeed":{"id":"3145856539","event_id":"457702655","user_id":null,"foreign_event_id":null,"type":"content","body":"<p>Audio Features
<br>

</p>
","website":null,"font":null,"source":"admin","sort_order":"0","start_date":null,"start_time":null,"end_time":null,"tweet_id":"","created":"2021-10-14 09:40:05","parent_splash_feed_id":null,"title":"","subtitle":"","image_url":"","temp_row":"0","raw_body":"0","options":[],"embed_code":null,"deleted":"0"}}],"type":"simple-container"},{"name":"Column 2","contain":1,"class":"","gid":923457559,"superType":"container","group":[{"element":"custom-block-3145856546","name":"Text","block_type":"content","gid":502011785,"superType":"","SplashFeed":{"id":"3145856546","event_id":"457702655","user_id":null,"foreign_event_id":null,"type":"content","body":"<p>
</p>
<p>Abigail Alexander, Matthijs Mars, Josh C. Tingey, Haoyue Yu, Chris Backhouse, Sravana Reddy, and Jussi Karlgren. \"Audio Features, Precomputed for Podcast Retrieval and Information Access Experiments.\" In Proceedings from the Conference and Labs of the Evaluation Forum (CLEF), 2021.
</p>
<p>
<br>

</p>
","website":null,"font":null,"source":"admin","sort_order":"0","start_date":null,"start_time":null,"end_time":null,"tweet_id":"","created":"2021-10-14 09:40:05","parent_splash_feed_id":null,"title":"","subtitle":"","image_url":"","temp_row":"0","raw_body":"0","options":[],"embed_code":null,"deleted":"0"}},{"element":"custom-block-3145856549","name":"Text","block_type":"content","gid":200275925,"superType":"","SplashFeed":{"id":"3145856549","event_id":"457702655","user_id":null,"foreign_event_id":null,"type":"content","body":"<p>Abigail Alexander, Matthijs Mars, Josh C. Tingey, Haoyue Yu. \"Audio-enhanced segment retrieval within the Spotify podcasts dataset.\" Technical report, University College London, 2021.
</p>
","website":null,"font":null,"source":"admin","sort_order":"0","start_date":null,"start_time":null,"end_time":null,"tweet_id":"","created":"2021-10-14 09:40:05","parent_splash_feed_id":null,"title":"","subtitle":"","image_url":"","temp_row":"0","raw_body":"0","options":[],"embed_code":null,"deleted":"0"}},{"element":"custom-block-3145856547","name":"Text","block_type":"content","gid":913571778,"superType":"","SplashFeed":{"id":"3145856547","event_id":"457702655","user_id":null,"foreign_event_id":null,"type":"content","body":"<p>https://github.com/trecpodcasts/podcast-audio-feature-extraction
</p>
","website":null,"font":null,"source":"admin","sort_order":"0","start_date":null,"start_time":null,"end_time":null,"tweet_id":"","created":"2021-10-14 09:40:05","parent_splash_feed_id":null,"title":"","subtitle":"","image_url":"","temp_row":"0","raw_body":"0","options":[],"embed_code":null,"deleted":"0"}}],"type":"simple-container"}],"type":"simple-container"}],"type":"simple-container"}]}]}]},{"element":"custom-block-3033911152","name":"Text","block_type":"content","gid":330106144,"superType":"","SplashFeed":{"id":"3033911152","event_id":"457702655","user_id":null,"foreign_event_id":null,"type":"content","body":"<p>
<br>

</p>
<p><a href=\"https://www.spotify.com/legal/\" target=\"_blank\" rel=\"noreferrer noopener\">Legal</a>           <a href=\"https://www.spotify.com/privacy/\" target=\"_blank\" rel=\"noreferrer noopener\">Privacy Center</a>         <a href=\"https://www.spotify.com/legal/privacy-policy/\" target=\"_blank\" rel=\"noreferrer noopener\">Privacy Policy</a>        <a href=\"https://www.spotify.com/legal/cookies-policy/\" target=\"_blank\" rel=\"noreferrer noopener\">Cookies</a>     
</p>
<p>
<br>

</p>
<p><a href=\"https://www.spotify.com/legal/privacy-policy/#s3\" target=\"_blank\" rel=\"noreferrer noopener\">About Ads</a>    <a href=\"https://www.spotify.com/legal/California-privacy-disclosure\" target=\"_blank\" rel=\"noreferrer noopener\">Additional CA Privacy Disclosures</a>
</p>
","website":null,"font":null,"source":"admin","sort_order":"0","start_date":null,"start_time":null,"end_time":null,"tweet_id":"","created":"2020-11-30 11:28:15","parent_splash_feed_id":null,"title":"","subtitle":"","image_url":"","temp_row":"0","raw_body":"0","options":[],"embed_code":null,"deleted":"0"}}]}]};
  </p>

-->

</div>  



  </body>
</html>
 

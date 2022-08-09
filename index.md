*Ann Clifton, Joana Correia, Md Iftekhar Tanveer, Edgar Tanaka, Jussi Karlgren, Ben Carterette, Rosie Jones*

Podcasts are a rapidly growing audio-only medium that involve new patterns of usage and new communicative conventions and motivate research in many new directions. To facilitate such research, we presented the Spotify English-Language Podcast Dataset in 2020 for use in the the TREC Podcasts Track shared tasks. Participants were asked to work on two tasks focusing on understanding podcast content, and enhancing the search functionality within podcasts. 

We have now released this dataset more widely to facilitate research on podcasts through the lens of speech and audio technology, natural language processing, information retrieval, and linguistics. We have recently added a Portuguese section of approximately equal size. 

The episodes span a variety of lengths, topics, styles, and qualities. Episodes were sampled from both professional and amateur podcasts ranging from material produced in a studio with dedicated equipment by trained professionals to material self-published from a phone app - these vary in quality depending on professionalism and equipment of the creator. Audio quality, topical content, and conversational format all vary over a wide range. The episodes include scripted and unscripted monologues, interviews, conversations, debate, and included clips of other non-speech audio material, some familiar from other published material, some novel with new emerging conventions. 

# GETTING ACCESS TO THE DATASET

We are happy to share the dataset for non-commercial use only to any research group with an academic affiliation and academic address, or with a track record of relevant research publications. Student projects are also welcome. 

Use [this form](https://docs.google.com/forms/d/e/1FAIpQLSca2WJ45uamUWJ-C5HxHe7a9M1FuiSQPqukTjL8o-vthbQtnA/viewform) to request the dataset.

After approval, we will send you a data sharing agreement to sign; after signature we will send you an access link for downloading the data. Approval of requests is a manual process so please allow at least two weeks to hear back from us.


# CONTENTS OF THE DATASET

The English-language dataset consists of 105,360 episodes from different podcast shows published between January 1, 2019 and March 1, 2020 on the Spotify platform which works out to about 50,000 hours of recorded speech, and over 600 million transcribed words. In 2022 we added a Portuguese section of 123,054 episodes published between September 9, 2019 and March 31, 2022, of more than 76,000 hours of recorded speech. The data set now consists of over 200,000 episodes. The episodes were randomly selected from our catalog and were constrained to be mostly speech (as opposed to music or ambient sound).

 
 Each of the episodes in the dataset includes an audio file, a text transcript, and some associated metadata. *Note that the data does <strong>not</strong> include listening data or other user or usage-related data.*
 
## Audio data
- Files in OGG format
- Median duration of an episode ~ 31.6 minutes
- Estimated size: ~2 TB for entire audio data set
## Metadata
- Extracted basic metadata file in TSV format with fields:
-- show_uri
-- show_name
-- show_description
-- publisher
-- language
-- rss_link
-- episode_uri
-- episode_name
-- episode_description
-- duration
 
## Episode RSS header files</div>
- ~1000 words with additional fields of potential interest, not necessarily aligned for every episode: channel, title, description, author, link, copyright, language, image
- Estimated size: 145MB total for entire RSS set when compressed.

## Transcripts
-	JSON format
- Average length is just under 6 000 words, ranging from a small number of extremely short episodes to up to 45 000 words. Two-thirds of the transcripts are between about 1 000 and about 10 000 words in length; about 1% or 1 000 episodes are very short trailers to advertise other content.
- Estimated size: 12GB for entire transcript set.

## Audio features
-	OpenSmile audio features:	eGeMAPS low level acoustic descriptors and functionals computed for overlapping 1.01s windows (75GB) saved in HDF5 format. 
-	Yamnet audio events:   	1024-dimensional embedding vectors for overlapping 0.96s segments for the podcasts (400GB) and Yamnet event class scores (60GB), saved in HDF5 format. 
  
  
  
<!-- Example of Transcript:

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

-->


# FAQ

## Is the dataset multilingual?

The data set is in English and in Portuguese, with some items that have leaked into the data set in other languages. We hope to release successive multilingual versions of the dataset in the future.

<!-- All information included in this dataset is pulled from content that is already publicly available on Spotify\u2019s service (i.e. metadata and content of published podcast episodes) -->

## Does the dataset contain user data?

No, the data set contains no information on searching, listening, recommendation or other data based on audience behaviour. 

## What were the TREC Podcasts Track Tasks?

We defined two tasks for participants in the TREC Podcasts Track.

### Task 1: Ad-hoc Segment Retrieval

Given an arbitrary keyword query, retrieve the jump-in point for relevant segments of podcast episodes. The best result would be a segment with very relevant content, which is also a good jump-in point for the user to start listening. We added some non-topical ranking criteria for the 2021 edition.

### Task 2: Summarization

Given a podcast episode with its audio and transcription, return a short snippet capturing the most important information in the content. 

[More information about the TREC Podcasts Track](https://trecpodcasts.github.io)

## What if there are inaccuracies in the data?

All RSS headers and audio are supplied by creators, and Spotify does not claim responsibility for the correctness of those data fields. All transcripts are generated using state of the art commercial automatic speech recognition and represent the audio content with a somewhat predictable level of errors. The language identification is based on creator-supplied data as well as automatic identification of language in the episode description and in spite of this we have found a number of non-English and non-Portuguese podcasts in the dataset. This level of inaccuracy in the data reflects the linguistic richness of the data and the multilingual reality of podcasts in general and are to some extent a feature, not a bug, of the dataset.  

## Who should be excited by this dataset?

Speech, NLP and Information Retrieval researchers who want to develop novel models on previously inaccessible streams of data. Also, any researchers interested in podcasts!

## Who organised the TREC shared task?
The TREC track was a collaboration between Spotify, NIST (the National Institute of Standards and Technology), CLARIN, Dublin City University, and TREC (the Text Retrieval Conference). All organising parties contributed to the task definition, the annotation standards, and the evaluation metrics. Spotify supplied the data. TREC supplied the infrastructure for participants to join the competition, submit their entries, and publish their system descriptions, and organizes a conference in November where participants share their results. NIST supplied the expert human annotators who will judge the participants' entries according to Spotify's annotation guidelines and metrics.

## What are some helpful resources we can look at if we want to learn more?

[The previous Spoken Document Retrieval task at TREC](https://pdfs.semanticscholar.org/57ee/3a15088f2db36e07e3972e5dd9598b5284af.pdf)

## Who can I reach out to if I have a question?

Contact the organizers: podcasts-challenge-organizers@spotify.com

# Citing the dataset

When referring to the data, please cite the following papers: 

## English Language Dataset

Ann Clifton, Sravana Reddy, Yongze Yu, Aasish Pappu, Rezvaneh Rezapour, Hamed Bonab, Maria Eskevich, Gareth Jones, Jussi Karlgren, Ben Carterette, and Rosie Jones. 2020. "100,000 Podcasts: A Spoken English Document Corpus". In *Proceedings of the 28th International Conference on Computational Linguistics (COLING)* 

[https://www.aclweb.org/anthology/2020.coling-main.519/](https://www.aclweb.org/anthology/2020.coling-main.519/)

`@inproceedings{clifton2020100,
  title={100,000 podcasts: A spoken {E}nglish document corpus},
  author={Clifton, Ann and Reddy, Sravana and Yu, Yongze and Pappu, Aasish and Rezapour, Rezvaneh and Bonab, Hamed and Eskevich, Maria and Jones, Gareth and Karlgren, Jussi and Carterette, Ben and Jones, Rosie},
  booktitle={Proceedings of the 28th International Conference on Computational Linguistics (COLING)},
  year={2020}
}`

<!--
> Podcasts are a large and growing repository of spoken audio. As an audio format, podcasts are more varied in style and production type than broadcast news, contain more genres than typically studied in video data, and are more varied in style and format than previous corpora of conversations. When transcribed with automatic speech recognition they represent a noisy but fascinating collection of documents which can be studied through the lens of natural language processing, information retrieval, and linguistics. Paired with the audio files, they are also a resource for speech processing and the study of paralinguistic, sociolinguistic, and acoustic aspects of the domain. We introduce the Spotify Podcast Dataset, a new corpus of 100,000 podcasts. We demonstrate the complexity of the domain with a case study of two tasks: (1) passage search and (2) summarization. This is orders of magnitude larger than previous speech corpora used for search and summarization. Our results show that the size and variability of this corpus opens up new avenues for research.
-->

## Portuguese Language Dataset 
Edgar Tanaka, Jussi Karlgren, Ann Clifton, Joana Correia, Sharmista Jat, Winstead Zhu, Md Iftekhar Tanveer, Rosie Jones. 2022.  "Cem Mil Podcasts: A Spoken Portuguese Document Corpus" (forthcoming)



# Published Research on the Spotify English Language Podcast Dataset
**If you have published material or analyses on the the Podcast Dataset, get in touch to have it included in this bibliography!** 

- **TREC 2020**: Rosie Jones, Ben Carterette, Ann Clifton, Maria Eskevich, Gareth JF Jones, Jussi Karlgren, Aasish Pappu, Sravana Reddy, and Yongze Yu. "TREC 2020 Podcasts Track Overview." *In the Twenty-Ninth Text REtrieval Conference Proceedings (TREC 2020)*. NIST Special Publication 1266. Ellen M. Voorhees and Angela Ellis (editors). 2021. [https://arxiv.org/abs/2103.15953](https://arxiv.org/abs/2103.15953)

- **TREC 2021**: 
Jussi Karlgren, Rosie Jones, Ben Carterette, Ann Clifton, Edgar Tanaka, Maria Eskevich, Gareth J. F. Jones, and Sravana Reddy. "TREC 2021 Podcasts Track Overview" *In the Thirtieth Text REtrieval Conference Proceedings (TREC 2021)*. NIST Special Publication 500-335. Ian Soboroff and Angela Ellis (editors). 2022. [https://trec.nist.gov/pubs/trec30/papers/Overview-Pod.pdf](https://trec.nist.gov/pubs/trec30/papers/Overview-Pod.pdf)

- **Audio Features:** Abigail Alexander, Matthijs Mars, Josh C. Tingey, Haoyue Yu, Chris Backhouse, Sravana Reddy, and Jussi Karlgren. \"Audio Features, Precomputed for Podcast Retrieval and Information Access Experiments.\" In *Proceedings from the Conference and Labs of the Evaluation Forum (CLEF)*, 2021. [https://github.com/trecpodcasts/podcast-audio-feature-extraction](https://github.com/trecpodcasts/podcast-audio-feature-extraction)

- **Workshop Report on Use Cases for Human Interaction with Audio Collections**: 
Gareth J. F. Jones, Maria Eskevich, Ben Carterette, Joana Correia, Rosie Jones, Jussi Karlgren, Ian Soboroff. "Report on the 1st Workshop on Audio Collection Human Interaction (AudioCHI 2022) at CHIIR 2022". SIGIR Forum 56:1. 2022. [https://sigir.org/wp-content/uploads/2022/07/p07.pdf](https://sigir.org/wp-content/uploads/2022/07/p07.pdf)

- **Information Retrieval Challenges for Podcasts**: Rosie Jones, Hamed Zamani, Markus Schedl, Ching-Wei Chen, Sravana Reddy, Ann Clifton, Jussi Karlgren, Helia Hashemi, Aasish Pappu, Zahra Nazari, Longqi Yang, Oguz Semerci, Hugues Bouchard, and Ben Carterette. "Current challenges and future directions in podcast information access." In *Proceedings of the 44th International ACM SIGIR Conference on Research and Development in Information Retrieval*. 2021. 

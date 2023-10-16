# MitigatingPopularityBiasUserStudy
The pre-processed dataset was created from the results of the user study conducted for the Master's Thesis by Robin Ungruh with the title: "Mitigating Popularity Bias in Music Recommender Systems: Effects on Fair Exposure, User Perception, and Motivation for Exploration".

The data in this repository was created by extracting and analyzing user profiles based on the top 50 of the participants' Spotify accounts, creating a more extensive user profile by expanding the data with Spotify recommendations. To create recommendations, we applied the collaborative filtering algorithm "RankALS" and the popularity bias mitigation algorithms "FA*IR" and "Calibrated Popularity".
The questionnaire scores are retrieved from the user's questionnaire responses during the study. For more information, we refer to the Master's Thesis: 

study_stats.csv includes all computed and measured metrics. study_stats_w_factors.csv includes the computed factors of the questionnaires. user_stats.csv is a subset of study_stats, including only the personal characteristics and answers to the "Musical Sophistication" and "Musical Engagement" questionnaires by Muellensiefen (2014). recommendation_similarities.csv includes the Similarity between the different playlists for each user. The directory recommendation_uris includes csv files with the Spotify-URIs of the recommendations for each user. choice_uris includes the Spotify-URIs for all choices made by the user based on the experimental task.
In study_stats and study_stats_w_facs, the metrics computed on the recommendations are highlighted by "rec", the ones computed on the user profiles by "prof" and the ones computed on the choices by "choice". The questionnaire questions are listed below. Reversed coded questionnaire scores are highlighted with an *. Questionnaires were typically measured on a 7-point Likert scale (3: Completely Agree, 2: Strongly Agree, 1: Agree, 0: Neither Agree Nor Disagree, -1: Disagree, -2: Strongly Disagree, -3: Completely Disagree).

Age:
Free-text comment

Gender:
Female; Male; Non-binary / third gender; Prefer not to say


Q_MusicalSophistication (Muellensiefen, 2014):
- MS01: I spend a lot of my free time doing music-related activities
- MS02: I enjoy writing about music, for example on blogs and forums
- MS03: If somebody starts singing a song I don't know, I can usually join in
- MS04: I can sing or play music from memory
- MS05: I am able to hit the right notes when I sing along with a recording
- MS06: I can compare and discuss differences between two performances or versions of the same piece of music
- MS07: I have never been complimented for my talents as a musical performer\*
- MS08: I often read or search the internet for things related to music
- MS09: I am not able to sing in harmony when somebody is singing a familiar tune\*
- MS10: I am able to identify what is special about a given musical piece
- MS11: When I sing, I have no idea whether I'm in tune or not\*
- MS12: Music is kind of an addiction for me - I couldn't live without it
- MS13: I don’t like singing in public because I’m afraid that I would sing wrong notes\*
- MS14: I would not consider myself a musician\*
- MS15: After hearing a new song two or three times, I can usually sing it by myself
- MS16: I engaged in regular, daily practice of a musical instrument (including voice) for ___ years (0; 1; 2; 3; 4-5; 6-9; 10 or more)
- MS17: At the peak of my interest, I practiced ___ hours per day on my primary instrument (0; 0.5; 1; 1.5; 2; 3-4; 5 or more)
- MS18: I can play ___ musical instruments (0; 1; 2; 3; 4; 5; 6 or more)


Q_MusicalEngagement (Muellensiefen, 2014):
- ME01: I spend a lot of my free time doing music-related activities
- ME02: I enjoy writing about music, for example on blogs and forums
- ME03: I'm intrigued by musical styles I'm not familiar with and want to find out more
- ME04: I often read or search the internet for things related to music
- ME05: I don't spend much of my disposable income on music\*
- ME06: Music is kind of an addiction for me - I couldn't live without it
- ME07: I keep track of new music that I come across (e.g. new artists or recordings)
- ME08: I have attended \_ live music events as an audience member in the past twelve months (0; 1; 2; 3; 4-6; 7-10; 11 or more)
- ME09: I listen attentively to music for __ per day (0-15; 15-30; 30-60; 60-90; 2hrs; 2-3hrs; 4hrs or more)

Q_Perceived_Popularity (Graus, 2021):
- PP01: The recommendations consist of popular tracks
- PP02: The recommendations consist of tracks that are currently played a lot by the media
- PP03: I do not think that the recommended tracks are very well known\*
- PP04: I believe that the majority of music listeners are familiar with the tracks in the recommendation
- PP05: The recommended tracks have been receiving a lot of attention by the media

Q_PerceivedFairness (Graus, 2021):
- PF01: The playlist has a good balance between popular and less popular items
- PF02: The playlist would be more balanced if \textit{more} popular items were included\*
- PF03: The playlist would be more balanced if \textit{less} popular items were included\*


Q_Discovery(Graus, 2021):
- D01: The recommendations broaden my taste
- D02: The recommendations deepen my taste
- D03: The recommendations allow me to discover new tracks to listen to
- D04: The recommendations allow me to refine my taste
- D05: The recommendations give me a new perspective on my musical taste



Q_Familiarity():
- F01: I am familiar with the recommended tracks
- F02: I do not know the tracks from the list\*
- F03: I already listen to the tracks that are recommended
- F04: I have heard the recommended tracks before 
- F05: The recommended tracks are already in my own playlists


Q_PerceivedRecommendationQuality(Knijnenburg, 2012):
- PQ01: I liked the items recommended by the system
- PQ02:The recommended songs fitted my preference
- PQ03:The recommended songs were well-chosen
- PQ04:The recommended songs were relevant
- PQ05:The system recommended too many bad songs\*
- PQ06:I didn’t like any of the recommended songs\*
- PQ07:The songs I selected were “the best among the worst"\*

Q_RecommendationSatisfaction (Graus, 2021):
- RS01: I am satisfied with the list of recommended tracks
- RS02: In most ways the recommended tracks are close to ideal
- RS03: The list of tracks recommendations meet my exact needs
- RS04: I would give the recommended tracks a high rating
- RS05: The list of tracks shows too many bad items\*
- RS06: The list of tracks is attractive
- RS07: The list of recommendations matches my preference

Q_ChoiceSatisfaction (Knijnenburg, 2012):
- CS01: I like the items I've chosen
- CS02: I was excited about my chosen items
- CS03: I enjoyed listening to my chosen items
- CS04: The items I listened to were a waste of my time\*
- CS05: The chosen songs fit my preference
- CS06: I know several songs that are better than the ones I selected\*
- CS07: Some of my chosen songs could become part of my favorites
- CS08: I would recommend some of the chosen songs to others/friends 

Q_PerceivedSystemEffectiveness():
- SE01: I would recommend the systems to others
- SE02: The system is useless\*
- SE03: The system makes me more aware of my choice options
- SE04: I make better choices with the system
- SE05: I can find better songs without the help of the system\*
- SE06: I can find better songs using the recommender system
- SE07: The system showed useful items



Q_OpennessSimilarRecommendations(Bogdanov, 2013):
- OS01: I would like to be recommended more songs similar to the one I were recommended
- OS02: I would like to receive more music recommendations that are similar in genre and style to the ones I just listened to
- OS03: I am interested in discovering more music from the same artists or bands that were recommended to me
- OS04: I would be likely to listen to more music from the same genre or style that was recommended to me
- OS05: I would appreciate it if the music recommender system suggests more songs that are similar in mood and tone to the ones I just listened to


Q_UseIntention(Pu, 2011):
- UI01: I will use this recommender again
- UI02: I will use this recommender frequently
- UI03: I will tell my friends about this recommender


Q_ChoiceListeningIntention(Pu, 2011):
- CLI01: I will listen to the songs that I have chosen again in the future
- CLI02: I will add the songs that I have chosen to my playlist


In study_stats:
- A_fair and A_cp are binary identifiers for the condition.
- attention is the response to the attention test, which was passed if the answer was 3
- Rank_Pl indicates on which rank the playlist was ranked by the user (1 being best, 3 being worst
- Validation_known is the response to "How many of the songs in the playlist do you know (in %) ?" and Validation_match is the response to "To what degree does the playlist match your personal preferences?", both measured on a scale from 0 to 100 and normalized to a scale from -50 to +50




References:

Bogdanov, D., Haro, M., Fuhrmann, F., Xambó, A., Gómez, E., & Herrera, P. (2013). Semantic audio content-based music recommendation and visualization based on user preference examples. Information Processing & Management, 49(1), 13-33.

Müllensiefen, D., Gingras, B., Musil, J., & Stewart, L. (2014). The musicality of non-musicians: An index for assessing musical sophistication in the general population. PloS one, 9(2), e89642.

Graus, M. P., & Ferwerda, B. (2021). The Moderating Effect of Active Engagement on Appreciation of Popularity in Song Recommendations. In Diversity, Divergence, Dialogue: 16th International Conference, iConference 2021, Beijing, China, March 17–31, 2021, Proceedings, Part I 16 (pp. 364-374). Springer International Publishing.

Ferwerda, B., Ingesson, E., Berndl, M., & Schedl, M. (2023, March). I Don’t Care How Popular You Are! Investigating Popularity Bias in Music Recommendations from a User’s Perspective. In Proceedings of the 2023 Conference on Human Information Interaction and Retrieval (pp. 357-361).

Knijnenburg, B. P., Willemsen, M. C., Gantner, Z., Soncu, H., & Newell, C. (2012). Explaining the user experience of recommender systems. User modeling and user-adapted interaction, 22, 441-504.

Pu, P., Chen, L., & Hu, R. (2011, October). A user-centric evaluation framework for recommender systems. In Proceedings of the fifth ACM conference on Recommender systems (pp. 157-164).

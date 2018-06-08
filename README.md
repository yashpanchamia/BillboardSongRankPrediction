# BillboardSongRankPrediction
# Background:
With the boom of internet, came a lot of opportunities for various types of industries such as financial markets, healthcare, retail, education etc. Music industry is not the one to be left behind, with the help of internet the audience base suddenly sky-rocketed. With millions of songs released every year in multiple languages, there was an obvious need for the user to know which song to listen to. This gave rise to various music chart archives such as Billboard.

# Potential Question(s):
Billboard determines its Hot-100 chart based on data collected from radio airplay, sales data and streaming data. In today’s era, if a song is on the Hot-100 chart, it is a hit, and so many artists want to know the whether their latest song will make the list or not. This gives rise to the following question:  
a)Is there a correlation that can be found between song features (refer feature description) and Hot-100 chart listing?  
b)If so, is there a way to predict whether a new song will land up on Hot-100 chart given the song features

# Target Variable(s):
a)  Will a song land on the Hot-100 chart? (Label Name: landed; values: Yes, No)  
b)  If so, at which rank will it land? (Label Name: Predicted Rank; values:1 to 100)

# Data sourced from:
•       Billboard weekly ranking list for the year 2017
        (http://www.billboard.com/charts/hot-100)  
•       Getting the features of the song such as artist, genre, loudness, danceability etc. (https://developer.spotify.com/web-api/)

# Analysis approach:
a)      Fetch and integrate data from two data sources mentioned above.  
b)      Cleaning the data by addressing missing values and filtering of redundant song versions.  
c)      Using Random Forest Classifier to predict if the song ends up on Billboard Hot-100 chart and to predict the rank of the song on the Hot-100 chart.  
d)      Evaluate the predictive model against the evaluation metrics to check the efficiency.

# Evaluation Metrics:
a)      Precision: A measure of a classifiers exactness.  
b)      Recall: A measure of a classifiers completeness  
c)      F-score: A weighted average of precision and recall.  
d)      ROC Curves: Like precision and recall, accuracy is divided into sensitivity and specificity and models can be chosen based on the balance thresholds of these values.  

# Feature Description:
|Feature Name   |Description|
| --- | --- |
|Acousticness   |A confidence measure from 0.0 to 1.0 of whether the track is acoustic. 1.0 represents high confidence the track is acoustic.|
|Danceability   |Danceability describes how suitable a track is for dancing based on a combination of musical elements including tempo, rhythm stability, beat strength, and overall regularity. A value of 0.0 is least danceable and 1.0 is most danceable. |
|Duration_ms    |The duration of the track in milliseconds.|
|Energy |       Energy is a measure from 0.0 to 1.0 and represents a perceptual measure of intensity and activity. Typically, energetic tracks feel fast, loud, and noisy. For example, death metal has high energy, while a Bach prelude scores low on the scale. Perceptual features contributing to this attribute include dynamic range, perceived loudness, timbre, onset rate, and general entropy.|
|Instrumentalness|      Predicts whether a track contains no vocals. "Ooh" and "aah" sounds are treated as instrumental in this context. Rap or spoken word tracks are clearly "vocal". The closer the instrumentalness value is to 1.0, the greater likelihood the track contains no vocal content. Values above 0.5 are intended to represent instrumental tracks, but confidence is higher as the value approaches 1.0.|
|Key | The key the track is in. Integers map to pitches using standard Pitch Class notation. E.g. 0 = C, 1 = C♯/D♭, 2 = D, and so on.|
|Liveness       | Detects the presence of an audience in the recording. Higher liveness values represent an increased probability that the track was performed live. A value above 0.8 provides strong likelihood that the track is live.|
|Loudness       | The overall loudness of a track in decibels (dB). Loudness values are averaged across the entire track and are useful for comparing relative loudness of tracks. Loudness is the quality of a sound that is the primary psychological correlate of physical strength (amplitude). Values typical range between -60 and 0 db.|
|Mode   | Mode indicates the modality (major or minor) of a track, the type of scale from which its melodic content is derived. Major is represented by 1 and minor is 0.|
|Speechiness |Speechiness detects the presence of spoken words in a track. The more exclusively speech-like the recording (e.g. talk show, audio book, poetry), the closer to 1.0 the attribute value. Values above 0.66 describe tracks that are probably made entirely of spoken words. Values between 0.33 and 0.66 describe tracks that may contain both music and speech, either in sections or layered, including such cases as rap music. Values below 0.33 most likely represent music and other non-speech-like tracks.|
|Tempo  |The overall estimated tempo of a track in beats per minute (BPM). In musical terminology, tempo is the speed or pace of a given piece and derives directly from the average beat duration.|
|Time_signature |An estimated overall time signature of a track. The time signature (meter) is a notational convention to specify how many beats are in each bar (or measure).|
|Valence |      A measure from 0.0 to 1.0 describing the musical positiveness conveyed by a track. Tracks with high valence sound more positive (e.g. happy, cheerful, euphoric), while tracks with low valence sound more negative (e.g. sad, depressed, angry).|
|Artists        |Name of the artists featured in the song|

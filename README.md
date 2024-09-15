# Pitch-ID-with-Machine-Learning
<h2>Problem:</h2>
From sign stealing to pitch tipping to Trajekt machines, pitch identification has been seen as an advantage for hitters since the beginning of baseball. Logic stands that the sooner the batter knows what pitch is coming, the more likely they'll be to adjust and exploit this knowledge. I used this principle to investigate how a machine learning model would go about identifying pitches. While humans observe the world around them much differently than machines, perhaps there's an approach they take that we can learn from. 

Here's how it went.

<h2>Approach:</h2>
I pulled Stat Cast data from all pitches thrown on September 13, 2024, filtered out all left hand pitchers (for consistency in side specific data), and then grouped pitches by fastball, breaking ball, and off speed pitches. I fed this data through a Random Forest Classifier and was somewhat surprised to find that it could identify pitch type with 98% accuracy - using only data collected immediataely upon release (i.e. velocity, spin rate, extension, etc.). I then analyzed what feature the model relied on the most to create such accurate prediction and found that it put 44% of its reliance on spin axis. This was 13% greater than the next most signficant feature (velocity). Diving into the spin axis data, I found that fastballs and off speed pitches share similar spin axis', typically between 210 degrees and 250 degrees, but the average breaking ball varied significantly with a spin axis of 87 degrees.

<h2>Insights:</h2>
The fact that breaking balls spin on a different axis from other pitches is by no means a revelation, but its relevance in pitch identification may be down played throughout the player development community. Hitters who are able to recognize different visual cues in spin axis will be able to gain an advatnage against the pitcher, and potentially exploit this advantage while they still have time to adjust, as it occurs immediately upon release. This is different than say velocity, whose equation (Distance / Time) inherently calls for *distance* to occur before recognition can occur. In the act of hitting, which relies in miliseconds, the need for distance in ones calculation can often render that approach useless.

<h2>Recommendations:</h2>
As an outsider of the player development community, I am not sure the degree to which conversations surround spin axis are occuring or how a performance coach would look to implement them. That being said, arming hitters with a familiarity on the subject, models or anaimations of different pitches rotating about common axis points (i.e. the mean values identified in the last page of the included PDF), and identifying visual cues within these animations may enhance a hitters awareness and approach in how they attempt to identify pitches sooner in their swing.

If this thoery has legs, or may already have legs within the game, pitchers may consider seeking an edge by minimizing the differences in their spin axis while shaping pitches. A pitcher who can disguise, or at least mitigate, visual cues indicative of their pitch axis and instead rely on other means of shaping pitches may discover unique ways to create diseption on the mound.

<h2>Limitations:</h2>
This data set is from one day, and while it occurs over 15 stadiums and 3,000+ pitches, it is still small in the grand scheme of potential pitchers invluded through out the league. Additionally, it condenses Stat Cast's 12 different pitch types into 3 broad categories. While I believe this is the correct approach for higher level investigations, some players may find use in accounting for all 12 pitch types if attempting to scout an opponent.

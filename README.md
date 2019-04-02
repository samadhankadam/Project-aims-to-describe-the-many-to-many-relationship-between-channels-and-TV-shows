Project aims to describe the many to many relationship between channels and TV shows

The project aims to display show-to-channel relationship is Many-to-Many. In other words, each
show might appear on many channels, and each channel might broadcast many shows.
The description of the data is as below
 TV show titles do not have spaces
 Channels have 3 letters
 TV show titles can appear multiple times, with different counts•
 A TV show and channel combination might appear multiple times•
 TV shows could appear on multiple channels•
 The output should have no commas or punctuation, only 1 space between the TV show title
• and number

The project aims at answering questions such as:
 What is the total number of viewers for shows on ABC?•
 What is the number of viewers for the BAT channel?•
 What is the most viewed show on ABC channel?•
 What are the aired shows on ZOO,NOX, ABC channels ?•

This has been implemented using Map Reduce Hive and Pig Spark programming





1) What is the total number of viewers for shows on ABC?
Map/Reduce - Advanced Join
make_join2data.py and make_data_join2.txt can be used to make the 6 input files used for this exercise.
 The join2_gennum*.txt files contain tv show names and viewer counts (show, viewer_count) and
 the join2_genchan*.txt files contain tv show names and the channel on which the show airs (show, channel). 
The objective is to return the number of viewers for shows on ABC.
•	The mapper emits (show, viewer_count) as the (key, value) for join2_gennum.txt files and emits (show, channel) as the (key, value) for join2_genchan.txt files when the channel is ABC.
•	The reducer receives the shuffled (key, value) pairs, aggregates the viewer_count values for all the same keys, and emits (show, viewer_total) for shows that have a (key, value) pair with ABC as the value.
Running join2_mapper.py and join2_reducer.py on the join2_gennum.txt and join2_genchan.txt files 
Results in the total_viewer_counts_output.txt file.




Adaptation of https://github.com/PRBonn/MapClosures

Allows for usage of MapClosures with an initial global map in addition to the local maps with the following:

MapClosures(Config) (Original) or MapClosures(Config, float ratio)

Where ratio denotes the ratio of initial global map size to local map size.

The global map is then passed in to MatchAndAddToDatabase with a negative id (-5 in the current kiss-slam implementation) to designate it as a global map.

When a map with negative ID is encountered by mapClosures, it uses a larger ORB feature extractor to account for the different size.

Contact Aditya Pulipaka: adipu@utexas.edu for any specific questions about these modifications.

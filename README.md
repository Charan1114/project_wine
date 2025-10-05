# project_wine

# first impression on data set, data is clean and balanced.
# there are various input features and output is a regression
# i think we need to normalize the input features in order to eliminate bias while we perform feature engineering and ensure correctness.
--
# regplot is best for checking linear relationship.
# boxplot is best for comparing distributions by categories.
# kdeplot is best for seeing how feature distributions shift with categories.

## here we have observed a key relation 
## previously we have derived a new feature that is ac_minus_volatile one it had moderate 0.52-0.53 with quality.
## but we have chose to move with different plan when i filtered the quality with max like 7-8 things changed. (it is just for the observation purpose)
## coor between ac_minus_volatile and quality decreased we have worked on it and observed.(we should train model with whole data)
## the narrow change between the quality like from 7-8 shows very little coorelation bet quality and new feature.
## so we have filtered the dataset with the 5-8 quality and observed the coorelation keenly.
## then we have realized that actually volatile acid has negative impact while rising with quality.
## so it showed strong coorelation when we minus volatile acid from alcohol the coor increased with quality.
## now we are observed that sulphate has 0.25 +ve impact on the quality when increasing.
## so we have decided to add it to the new feature to test impact.
## because there is no significant impact shown by sulphate we just scaled it and left
# and our best random forest model has got 0.55 r2 score
# In this dataset imput feature impact on quality is only about 60 percent we cant enhance it furthur
# And in last we have achieved 0.55 as the highest r2 score through fine tuning random forest and named the model as best_random_forest.pkl.

# also we have dumped modifies csv to the processed folder
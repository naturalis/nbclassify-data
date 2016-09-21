This folder contains results of 4 analyses:
- 3 have been done using 5 to 50 photos per species for k=2, k=5 and k=10. P. polytes was split into a male and female group
- 1 has been done using 20 to 50 photos per species for k=2. P. polytes was treated as one group

Each analysis has 4 folders:
- train: contains training data for each subanalysis
- ann: contains neural networks created from the training data
- test: contains data used for testing the ann
- results: contains results of the validation
  - genus (exp) and species (exp) are the expected result, this is the classification as done by the expert
  - when species (exp) is empty, there was only one species for that particular genus
  - genus (class) and species (class) contain the results of the ann
  - Match shows weather of not there is a complete match between expected and classification results.
  - section can be ignored, as this was not used in these analyses

The Results.xlsx contains a summary of the results of all analyses, including graphs and tables with outcomes per species/genus/analysis

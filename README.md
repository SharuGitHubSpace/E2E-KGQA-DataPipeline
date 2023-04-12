# E2E-KGQA-DataPipeline


Steps to get the Goldendataset for Model training 
# Step 1 : Split the Train(1750)  - Val(250) - Test(500) 
          # conditions are category  = movies , keep questions only that are in answer entity type 'entity' and 'string'
        ###  ###  ###  ###  ###  ###  LOOP             ###  ###  ###  ###
# Step 2 : Follow steps to get the DS for Set 1 
           # loop every question 
           # Extract all QID from question 
           # Extract all Answer id from question
           # write to a file QID-AID-Log.xslx (With reference to train / val / test) every qid - aid , if there are 2 qid make two rows Q_QID1 - A_QID1 ,            
           # Log all combinations
           
# Step 3 : SPARQL - Find if the QID -AID pair has a  predicates from SPARQL
           # if there is match , put the QID-AID pair and s-p-o in the triplet_csv.xslx
           # Copy the QID1 and QID2 and AID to entity_csv.xslx
           # copy the predicate to predicate_csv.xlsx
           # Outcome of this step is the S -> P -> O triplets triplet_csv_master.xlsx

# Step 4 : # From last step map literals to the unique QID and remove duplicates  call it literal_csv.csv

# Step 5 : # Prepare the vlookup in the excel 

This code is used to create the data for the Model training. The data is loaded from the Mintaka json dataset and the Train, Validation and Test dataset. The output of the pipeline is Entities.csv , Triple.csv and Predicate.csv which is fed for Model Training.


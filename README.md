# iNAGO_Project

Conversational Recommender System Project Instruction

All the previous capstone weekly meeting slides can be found in this folder: https://drive.google.com/open?id=13HpdSRvGXE2o65obFEO4XRMotlKH9g5E

All the documentations for the project can be found in this folder:
https://drive.google.com/drive/folders/1Z7IQ37hP4zbmX1uilBK-VBJrxUnq7dJP?usp=sharing

The Final Design Specification document can be found using this link: https://docs.google.com/document/d/1IqQp5szMM--H6LMn1vEntEDKenbILv2izSJUxu0kGqk/edit?usp=sharing

*All data files will be located at  ../data/

<b>Data preprocessing & Generation</b>
<br>This file processes the Toronto businesses data and the review data, filtered out businesses that are non-restaurants by identifying the selected keywords contained in the restaurant categories. 

Data preprocessing code: 
- data_processing.ipynb

Imported Data files:
- toronto_reviews.csv
- businesses_final_toronto.csv

Cleaned exported data files:
- Cleaned_Toronto_Reviews.json
- Cleaned_Toronto_Business.json

<b>Project data generation (for Recommender System)</b>
<br>Run following code for data files generation:
<br>`python projectData_generation.py –data_dir ../data/ --data_name Cleaned_Toronto_Reviews.json`

Data file generations code: 
- projectData_generation.py

Imported data files:
- Cleaned_Toronto_Reviews.json

Generated data files:
- icDictionary.json
- ipDictionary.json
- isDictionary.json
- idDictionary_yongefinch.json
- idDictionary_bloorbathurst.json
- idDictionary_spadinadundas.json
- idDictionary_queenspadina.json
- idDictionary_blooryonge.json
- idDictionary_dundasyonge.json
- rtrain.npz
- icmatrix.npz
- IKbased_II_similarity.npy
- UI_prediction_matrix.npy

<b>Explanation generation</b>
<br>This code reads in the Toronto business data file and generate 3 explanation phrases for each business. Detailed logic behind the generation of the explanation phrases can be found in the Explanation documentation. 

Data preprocessing code: 
- data_processing.ipynb

Imported data files:
- Export_TorontoData.json

Exported explanation data file:
- Toronto_explanation.json

<b>Conversational Recommender System API</b>
<br>The file reads in all the generated data files, run the recommender system and connects it with an API. Different functions are enabled through different endpoints. Details for the design of these endpoints and user-system interaction logic can be found in the API documentation. 

API code: 
- convSys_API.ipynb

Imported Data files:
- Toronto_explanation.json
- All the data files generated from Section 2
 
<b>Conversational Recommender System Middle tier (fulfillment agent)</b>
<br>This part of the code handles the middle tier of the project, which matches the user’s intents to the correct response, and send retrieve the corresponding responses for the intent. 
 
Fulfillment code: 
- index.js

<b>Conversational Recommender System front end (Google Dialog Flow agent)</b>
<br>Use the following steps to import the capstone Google Dialog Flow project. 

Dialogflow project to import:
- Inago-Capstone-Recsys.zip

<b>Additional files</b>
<br>These files contain the research code for the project but do not directly contribute to the operation of the conversational recommender system. 

<b>allMethods_CrossValidation.ipynb:</b>
<br> This research code compares all different algorithms the group considered for the recommender system. The cross-validation process was performed. All the functions were not formatted, the computation time is long. However, it gives a brief overview of all the different attempts the group used for the recommender system. 

<b>algorithmSelection_userStudy.ipynb</b>
<br> This research code was used for computing the first user study operated by the group. Where the users will be exposed with 5 different algorithms used for making restaurant recommendations. 

<b>similarityCalculation_analysis.ipynb</b>
<br> This file contains the research code for analysing different ways of computing the similarity matrices for user-based and item-based collaborative filtering methods for restaurant recommendations. 

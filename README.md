# Isnad Datasets

The repository contains CSV files with information on hadiths and hadith narrators and Jupyter Notebooks that read this data and turn them into graphs. The graphs are then edited on [GraphSpace](http://www.graphspace.org/), and then used for the interactive network graph visualization app. 

This was developed as part of the capstone project for the Graduate Certificate in Digital Humanities at Northeastern University, [Muhaddithat Networks](https://muhaddithat.net). 

## Data model:
- URL: URL for the hadith
- isnad: comma-separated list of numeric IDs corresponding to the isnad chain. 
- notes: data entry notes 
- ID: number representing the hadith or the hadith narrator. For the hadith narrators, this corresponds to the ID assigned by muslimscholars.info.
- displayname: the narrator's shortened name, with diacritics, that will be displayed on the node on the graph.
- fullname: the narrator's full name in English with diacritics.
- searchname: the narrator's full name without diacritics.
- arabicname: the narrator's full name in Arabic.
- gender: the narrator's gender.
- info: brief description of the narrator.

## Data sources:
- [muslimscholars.info](https://muslimscholars.info/)
- [Sunnah.com](https://sunnah.com/)

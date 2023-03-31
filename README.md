# Isnad Datasets

This repository contains CSV files with information on hadiths and hadith narrators and Jupyter Notebooks that read this data and turn them into graphs. It was developed as part of the capstone project for the Graduate Certificate in Digital Humanities at Northeastern University, [Muhaddithat Networks](https://muhaddithat.net). 

In order to make a network graph for each of the selected muhaddithat, I first created a CSV file, [hadiths.csv](https://github.com/muhaddithat/isnad-datasets/blob/main/data/hadiths.csv), containing a list of hadiths with their corresponding isnads (narration chains). A second CSV file, [found here](https://github.com/muhaddithat/isnad-datasets/blob/main/data/variousnarrators.csv), lists information about the hadith narrators (their full names in Arabic and English, gender, and brief one-line bios).The ID numbers I use for the scholars in my dataset the same as the ones used in [muslimscholars.info](https://muslimscholars.info/) for the sake of consistency and ease of looking up the scholars.

The Jupyter notebook in this repository reads these files and outputs a graph. To make the social network graphs, I used [GraphSpace](http://www.graphspace.org/), which offers both a Python library and a web-based platform. I used the Python library to read the data from the CSV files, create it into graph objects, and export them to the web-based platform. There, I can visualize the graphs and decide how to position the nodes and edges so that they are easily understood. Graphspace records the positions and edges of these nodes, along with the other information initially received from the Python portion, and exports them into JSON files representing the graph, which are stored in [another repo containing the app framework](https://github.com/muhaddithat/interactive-graph-app). 

All of the hadiths selected are checked for authenticity via their label (determined by Muslim scholars of hadith over the centuries) as sahih (sound) or hasan (good). For each of the narrators, I selected a few of the hadiths they narrated, favoring hadiths with other women narrators in their isnads. Therefore, this dataset overrepresents hadiths narrated by Muslim women, as these are the scholars whose work, lives, and contribution to the hadith tradition I aim to emphasize.  Therefore, any social network analysis done on this data will not be telling the full picture, since my data does not equitably represent the entire community of hadith scholars. 


## Data model:
- **URL**: URL for the hadith
- **isnad**: comma-separated list of numeric IDs corresponding to the isnad chain. 
- **notes**: data entry notes 
- **ID**: number representing the hadith or the hadith narrator. For the hadith narrators, this corresponds to the ID assigned by muslimscholars.info.
- **displayname**: the narrator's shortened name, with diacritics, that will be displayed on the node on the graph.
- **fullname**: the narrator's full name in English with diacritics.
- **searchname**: the narrator's full name in English without diacritics.
- **arabicname**: the narrator's full name in Arabic.
- **gender**: the narrator's gender.
- **info**: brief description of the narrator.

## Data sources:
- [muslimscholars.info](https://muslimscholars.info/)
- [Sunnah.com](https://sunnah.com/)

# IT496: Introduction to Data Mining (IDM)
# Course Project - 4

Project on Book Depository Dataset (Dataset-4)

### DOPE-a-MINE (Team-18)
* Maulik Thakkar (202101415)
* Maharshi Pipaliya (202101210)
* Sameer Sonara (202101489)
* Harshil Patel (202101019)
* Kunj Kapadiya (202103018)

### Abstract :
This dataset provides valuable insights into the world of books available on a book depository, encompassing a wealth of information, including titles, descriptions, unique identifiers, publication details, and various attributes related to their physical characteristics. One of the significant attributes is the format of these books, which often influences their handling, shipping, and reader experience. The format may range from hardcover to paperback, e-books, and other variants, each tailored to meet different reader preferences and industry demands.

### Dataset Description :
This dataset contains a large collection of books that are indexed/scraped from bookdepository.com, not the actual contents of the books but their metadata like title, description, category(ies), cover image, physical attributes, and others. This dataset could be used for natural language processing, text classification, computer vision, and other machine learning tasks. Below is the list of fields of the dataset:

1. ``[int]`` **authors** - Author(s) of the book (*authors.csv* containing the mapping)
1. ``int`` **bestsellers-rank** - Bestsellers rank of the book on the website
1. ``[int]`` **categories** - Categories (and genres) of the book (*categories.csv* containing the mapping)
1. ``str`` **description** - Description of the book
1. ``float`` **dimension-x** - X-Dimension of the book (in cms)
1. ``float`` **dimension-y** - Y-Dimension of the book (in cms)
1. ``float`` **dimension-z** - Z-Dimension of the book (in mms)
1. ``str`` **edition** - Edition of the book
1. ``str`` **edition-statement** - Edition statement of the book
1. ``str`` **for-ages** - Suitable (or recommended) age(s) of the readers
1. ``int`` **format** - Format of the book (*formats.csv* containing the mapping)
1. ``int`` **id** - Unique identifier of the data tuple
1. ``str`` **illustrations-note** - Note on the illustrations contained in the book
1. ``str`` **image-checksum** - Book's cover image checksum
1. ``str`` **image-path** - Book's cover image file path
1. ``str`` **image-url** - Book's cover image URL
1. ``str`` **imprint** - Imprint (i.e. publisher's specialized subsidiary) of the book
1. ``str`` **index-date** - Date on which the data tuple was indexed/scraped from the website
1. ``str`` **isbn10** - ISBN-10 number of the book
1. ``str`` **isbn13** - ISBN-13 number of the book
1. ``str`` **lang** - Language in which the book is written
1. ``str`` **publication-date** - Publication date of the book
1. ``int`` **publication-place** - Publication place of the book (*places.csv* containing the mapping)
1. ``float`` **rating-avg** - Average rating of the book on the website (b/w 1 & 5)
1. ``int`` **rating-count** - Number of ratings of the book on the website
1. ``str`` **title** - Title of the book
1. ``str`` **url** - Relative URL of the book on the website (https://bookdepository.com + url)
1. ``float`` **weight** - Weight of the book (in gms)

### Key Insights :

- Paperback, Hardback, and CD constitute about 98% of all the formats in the dataset. So, we will consider only these three formats for our classification problem.
- Based on the scatter plots, it's evident that CDs have equal dimension-x and dimension-y values, tend to have smaller dimension-z values, and are relatively lightweight. In contrast, hardback books exhibit significantly higher weights. Paperback books, on the other hand, fall in between with intermediate dimension-z and weight values. Also, paperback books show significantly higher dimension-y values. While hardback books, on the other hand, have middle dimension-y value.
- We also encounter a classification challenge wherein we aim to categorize readers into different age groups based on the information provided in the book titles and descriptions. However, the "for-ages" column, which could have been a valuable source of information for this task, contains mostly missing values (~93%), rendering it unsuitable.
- We also found a significant number of books falling into the following categories through EDA:
1. Anthologies (non-poetry)
1. Children's Fiction
1. Contemporary Fiction
1. Graphic Novels,Anime & Manga
1. Horror
1. Miscellaneous Items
1. Science Fiction
1. Study & Learning Skills: General
1. Teaching Resources & Education

### Classification Problems :

- The classification problem we chose involved classifying a book's format based on the attributes dimension-x, dimension-y, dimension-z, and weight.
- For the book format classification, we used three different algorithms: Logistic Regression, Decision tree classifier, and Random forest classifier. With their accuracies being,
1. Logistic Regression: 78.12%
2. Decision tree classifier: 88.75%
3. Random forest classifier: 90.03%
- Another classification problem that may be done on this dataset would be classifying the books categories or genres based on attributes such as title, description, and authors. However, the computational resources and technical expertise required for such a task were beyond the scope of this project.

### References :

- Terminologies and understanding of the dataset : [kaggle.com](https://www.kaggle.com/datasets/sp1thas/book-depository-dataset)
- Model classification and optimization : [scikit-learn.org](https://scikit-learn.org/stable/supervised_learning.html)

### Acknowledgements :

We would like to express our sincere gratitude and appreciation to [Prof. Arpit Rana](https://www.daiict.ac.in/faculty-details/3407) for his invaluable support and contributions to this project and that to Vipasha Vaghela, Himanshu Beniwal, and Aksh Patel.

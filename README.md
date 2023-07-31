<h1> Project Summary </h1>

This dataset consists of TV shows and movies available on Netflix as of 2021. The dataset is collected from Flixable which is a third-party Netflix search engine. In 2018, they released an interesting report which shows that the number of TV shows on Netflix has nearly tripled since 2010. The streaming service's number of movies has decreased by more than 2,000 titles since 2010, while its number of TV shows has nearly tripled. We will be exploring other such insights obtained from the same dataset along with some clustering model implementation.


<h1> Problem Statement </h1>

In this project, we are required to do the following:
* Exploratory Data Analysis.
* Finally and most importantly, clustering similar content by matching text-based features.


<h1> Getting to Know the Data </h1>

* There are 7787 rows and 12 columns in the dataset.
* The issue of duplicate values is not there in the dataset.
* The are is a total of 3631 missing/null values in the dataset. The missing values are there in the 'director', 'cast', 'country', 'date_added' and 'rating' columns only.


<h1> Understanding The Variables </h1>

1. **show_id**: The unique ID for every Movie/TV show.
2. **type**: An identifier depicting whether the record is a movie or a TV show.
3. **title**: The title of the show.
4. **director**: The director of the show.
5. **cast**: The actors involved.
6. **country**: The country of production.
7. **date_added**: The date it was added on Netflix.
8. **release_year**: The actual release year of the show.
9. **rating**: The rating of the show.
10. **duration**: The total duration in minutes or number of seasons.
11. **listed_in**: The genre of the show.
12. **description**: The description or the summary of the show.


<h1> Data Wrangling </h1>

* The null/missing values were taken care of by imputing with suitable values.
* The values under 'date_added' were parsed into datetime objects.
* The values under 'cast' and 'listed_in' were converted from string to list.
* Four new columns called 'month_added', 'year_added', 'lead_actor', 'main_genre' and 'main_country' were created.


<h1> Data Visualization & Exploratory Data Analysis </h1>

The following insights were extracted:

* There are more Movies than TV Shows. Of all the contents, 69.1% are Movies and 30.9% are TV Show.
* After the year of 2015, there has been rapid increase in the influx of both: Movies and TV Shows.
* There is a sharp rise in the number of new Movies being added, from 2015 to 2019. For the number of new TV Shows being added each year, there is a steady increase.
* In the year of 2020, the number of new Movies added was less than the previous year.
* Most number of Movies were added to Netflix in the month of January, followed by December and October
* Most number of TV Shows were added to Netflix in the month of December.
* Some of the most popular genres for the movies are: Dramas, Comedies, Documentaries and Action & Adventure.
* Some of the most popular genres for the movies are: International TV Shows, Crime TV Shows, Kid's TV Shows, British TV Shows, Docuseries and Anime.
* Most of the contents for Netflix is produced by United States, followed by India, United Kingdom, Canada, Japan, France, South Korea and Spain.
* 'TV-MA' is the most common rating for both the Movies and TV Shows.
* Most of the Movies are of 90 minutes and most of the TV Shows have 1 season.


<h1> Hypothesis Testing </h1>

* `Chi-Square Test` is used to check whether there is relation between the 'type' of the content and the 'rating' of the content.
* `Chi-Square Test` is used to check whether there is relation between the 'type' of the content and the 'main_genre' of the content.
* `Chi-Square Test` is used to check whether there is relation between the 'main_genre' of the content and the 'rating' of the content.


<h1> Feature Engineering & Data Pre-processing </h1>

The following steps were taken:

* Lower Casing
* Removing Punctuations
* Removing Non-ASCII Characters
* Expand Contraction
* Removing Stopwords & Removing White spaces
* Text Normalization
* Tokenization
* Text Vectorization
* Dimesionality Reduction


<h1> ML Model Implementation </h1>

The following models were fitted over the data:

* K-Means Clustering
* Agglomerative (Hierarchical) Clustering


<h1> Conclusion </h1>

* During the Exploratory Data Analysis, it was observed that on Netflix:
  - There are more number of Movies compared to TV Shows;
  - The overall number of Movies and TV Shows have only increased over the years;
  - Usually in the month of December, more number of contents are added;
  - The most popular genre for the Movies is Drama and the most popular genre for the TV Shows is International TV Show.
  - Some of the most content producing countries are US, India, UK, Canada, Japan, France, South Korea and Spain.
  - The most common rating for both the Movies and the TV Shows is TV-MA.
  - Most of the Movies have a duration of 90 minutes and most of the TV Shows have only 1 season.

* The textual data was preprocessed by performing actions such as removing non-ASCII characters, removing stopwords, lemmatization, tokenization, vectorization, etc.

* The dimensionality of the preprocessed data was also reduced using the Principal Component Analysis.

* K-Means Clustering was implemented to form 9 clusters. The optimum number of clusters was decided upon through Silhouette Analysis.

* Agglomerative (Hierarchical) Clustering was implemented to form 5 clusters. The optimum number of clusters was decided upon with the help of a Dendrogram.

* The average Silhouette Score for the K-Means Clustering was higher than the average Silhouette Score for the Agglomerative Clustering. So, the K-Means Clustering Model was selected as the final model.

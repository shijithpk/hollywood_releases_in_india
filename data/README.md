Realised I need to explain what some of the column labels in **india_release_check_v20.csv** are, this is the csv which my analysis is based on. Most of the data in the csv is from [the-numbers.com](http://the-numbers.com) unless stated otherwise.

The columns of note in the csv, the ones I ended up using in the story are **domestic_box_office**, **released_in_india_2nd_check**, **genres_imdb_extended** and **distributor_us**.

- **number** : Part of an internal file numbering system i used, dont worry about this
- **year** : Release year of a movie
- **title** : Title of a movie, it's usually the one used in the US market
- **domestic_box_office** : US box office earnings. So domestic here refers to the US
- **production_budget** :  Production budget info where available
- **domestic_release_date** : Release date in the US
- **domestic_distributor** : Company that released movie in US
- **mpaa_rating** : Self-explanatory
- **franchise** : Just some additional info provided by the-numbers.com, dont worry about it
- **source** : Whether the movie is based on a book, game or it's an original screenplay etc.
- **genre** : Self-explanatory. This column used genre info from the-numbers.com. The problem
            here is that some movies need to be placed in multiple genres, while the-numbers.com
            only assigns one. So ended up not using this.
- **production_method** : Whether it's live action, animation etc.
- **creative_type** : Don't really get what this label from the-numbers was for
- **production_companies** : This has a list of the various companies involved in the production of a movie. The companies are separated by comma.
- **production_countries** : Countries where production took place or the countries which companies belonged to, not really sure, didn't use it anyway
- **released_in_india_2nd_check** : Yes or No depending on whether a movie was released in India or not. This is actually the main column in the csv. This was filled based on whether the title was present in the BookMyShow list. Additional checking was also done using Google, news reports, critics reviews etc.
- **production_budget_bins** : Tried to group the movies in 'bins' according to the production budget
- **domestic_box_office_bins** : Tried to group the movies in 'bins' according to US box office earnings
- **director** : Self-explanatory
- **genres_imdb_final** : This has upto 3 genres listed for each movie, info was taken from IMDB data dumps available at [https://datasets.imdbws.com/](https://datasets.imdbws.com/). Realised there was more complete genre data available on the IMDB website, the website has sometimes more than 3 genres listed for a movie. I ended up not using this column.
- **languages_imdb** : Languages spoken in the movie according to the IMDB website
- **id_imdb** : IMDB's internal id for each movie
- **genres_imdb_extended** : Genres for each movie according to the IMDB website, scraped using the [IMDbPy](https://imdbpy.sourceforge.io/) library. This is the column I ended up using in the story.
- **distributor_us** : Different US distributors are part of different studios. We found which studio each distributor belonged to, and if it's one of the major studios, the name of the studio was listed here. This column was used in the story too.

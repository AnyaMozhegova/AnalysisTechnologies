# Задание

Разработать XML-формат для представления информации о художественных фильмах. Необходимо представить название, информацию о жанре(ах), режиссёре(ах), композиторе(ах), актерском составе, дате выхода, кассовых сборах, возрастных ограничениях, количестве зрителей, языке оригинала.

# Выполнение

1. В разработанном формате представить расписание текущей недели. (1 балл)
```xml
<?xml version="1.0" encoding="UTF-8"?>
<movies>
    <movie>
        <title>Inception</title>
        <genres>
            <genre>Sci-Fi</genre>
            <genre>Thriller</genre>
        </genres>
        <directors>
            <director>Christopher Nolan</director>
        </directors>
        <composers>
            <composer>Hans Zimmer</composer>
        </composers>
        <cast>
            <actor>Leonardo DiCaprio</actor>
            <actor>Joseph Gordon-Levitt</actor>
            <actor>Ellen Page</actor>
            <actor>Tom Hardy</actor>
            <actor>Ken Watanabe</actor>
            <actor>Cillian Murphy</actor>
        </cast>
        <release_date>2010-07-16</release_date>
        <box_office>829895144</box_office>
        <age_rating>PG-13</age_rating>
        <audience_count>10000000</audience_count>
        <original_language>English</original_language>
    </movie>
    <movie>
        <title>Interstellar</title>
        <genres>
            <genre>Sci-Fi</genre>
            <genre>Drama</genre>
        </genres>
        <directors>
            <director>Christopher Nolan</director>
        </directors>
        <composers>
            <composer>Hans Zimmer</composer>
        </composers>
        <cast>
            <actor>Matthew McConaughey</actor>
            <actor>Anne Hathaway</actor>
            <actor>Jessica Chastain</actor>
            <actor>Michael Caine</actor>
            <actor>Casey Affleck</actor>
        </cast>
        <release_date>2014-11-07</release_date>
        <box_office>677471339</box_office>
        <age_rating>PG-13</age_rating>
        <audience_count>8000000</audience_count>
        <original_language>English</original_language>
    </movie>
    <movie>
        <title>Pulp Fiction</title>
        <genres>
            <genre>Crime</genre>
            <genre>Drama</genre>
        </genres>
        <directors>
            <director>Quentin Tarantino</director>
        </directors>
        <composers>
            <composer>Various</composer>
        </composers>
        <cast>
            <actor>John Travolta</actor>
            <actor>Uma Thurman</actor>
            <actor>Samuel L. Jackson</actor>
            <actor>Bruce Willis</actor>
        </cast>
        <release_date>1994-10-14</release_date>
        <box_office>213928762</box_office>
        <age_rating>R</age_rating>
        <audience_count>5000000</audience_count>
        <original_language>English</original_language>
    </movie>
    <movie>
        <title>The Dark Knight</title>
        <genres>
            <genre>Action</genre>
            <genre>Crime</genre>
        </genres>
        <directors>
            <director>Christopher Nolan</director>
        </directors>
        <composers>
            <composer>Hans Zimmer</composer>
            <composer>James Newton Howard</composer>
        </composers>
        <cast>
            <actor>Christian Bale</actor>
            <actor>Heath Ledger</actor>
            <actor>Aaron Eckhart</actor>
            <actor>Michael Caine</actor>
            <actor>Maggie Gyllenhaal</actor>
        </cast>
        <release_date>2008-07-18</release_date>
        <box_office>1004558444</box_office>
        <age_rating>PG-13</age_rating>
        <audience_count>12000000</audience_count>
        <original_language>English</original_language>
    </movie>
    <movie>
        <title>The Grand Budapest Hotel</title>
        <genres>
            <genre>Comedy</genre>
            <genre>Drama</genre>
        </genres>
        <directors>
            <director>Wes Anderson</director>
        </directors>
        <composers>
            <composer>Alexandre Desplat</composer>
        </composers>
        <cast>
            <actor>Ralph Fiennes</actor>
            <actor>Tony Revolori</actor>
            <actor>F. Murray Abraham</actor>
            <actor>Adrien Brody</actor>
            <actor>Willem Dafoe</actor>
        </cast>
        <release_date>2014-03-28</release_date>
        <box_office>174600318</box_office>
        <age_rating>R</age_rating>
        <audience_count>3000000</audience_count>
        <original_language>English</original_language>
    </movie>
</movies>
```

# Задание

Разработать XML-формат для представления информации о художественных фильмах. Необходимо представить название, информацию о жанре(ах), режиссёре(ах), композиторе(ах), актерском составе, дате выхода, кассовых сборах, возрастных ограничениях, количестве зрителей, языке оригинала.
Основная структура документа
 - Корневой элемент ```<movies>``` содержит все данные о фильмах. Внутри него для каждого фильма создается элемент <movie>, в котором собрана информация о конкретной киноленте.
 - Элементы внутри ```<movies>```. Каждый ```<movies>``` включает несколько вложенных элементов, каждый из которых описывает одну характеристику фильма:
    1. Название фильма (<title>)
       Содержит название фильма, например, <title>Inception</title>.
    2. Жанры (<genres>)
       Элемент <genres> включает один или несколько <genre>, указывающих на жанры фильма. Например, для фильма "Inception" жанры указаны как <genre>Sci-Fi</genre> 
       и <genre>Thriller</genre>. Это позволяет фильму принадлежать сразу к нескольким жанрам.
    3. Режиссеры (<directors>)
       Этот элемент содержит один или несколько <director>, указывающих режиссеров фильма. Например, <director>Christopher Nolan</director>. Это удобно для 
       фильмов,    где над проектом работало несколько режиссеров.
    4. Композиторы (<composers>)
       Аналогично режиссерам, элемент <composers> содержит один или несколько <composer>, которые указывают композиторов, создавших саундтрек к фильму.
    5. Актерский состав (<cast>)
       Элемент <cast> содержит список <actor>, представляющий актеров, участвовавших в фильме. Например, <actor>Leonardo DiCaprio</actor>. В примере указано 
       разное количество актеров для разных фильмов, что позволяет хранить большие актерские составы.
    6. Дата выхода (<release_date>)
       Содержит дату выхода фильма в формате YYYY-MM-DD, например, <release_date>2010-07-16</release_date>.
    7. Кассовые сборы (<box_office>)
       Отображает мировые кассовые сборы фильма в долларах, например, <box_office>829895144</box_office>. Использование числового значения помогает легко 
       выполнять запросы для фильмов с определенным уровнем кассовых сборов.
    8. Возрастной рейтинг (<age_rating>)
       Содержит возрастное ограничение для фильма, например, <age_rating>PG-13</age_rating>. Это позволяет фильму хранить информацию о возрастных ограничениях для 
       аудитории.
    9. Количество зрителей (<audience_count>)
       Указывает примерное количество зрителей, посмотревших фильм, например, <audience_count>10000000</audience_count>. Этот элемент хранит числовую информацию о 
       популярности фильма.
    10. Язык оригинала (<original_language>)
         Этот элемент указывает, на каком языке изначально был снят фильм, например, <original_language>English</original_language>. Это полезно для каталогов, 
         которые хранят мультиязычные фильмы.

# Задачи
1. В разработанном формате представить информацию о 5 фильмах (минимум). (1 балл)
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
2.  Разработать xPath-запросы (2 балла):
  a)      Получить все фильмы указанного жанра (например, "Sci-Fi").
```xml
       //movie[genres/genre="Sci-Fi"]
```
  b)      Получить все фильмы с актерским составом белее пяти человек.
```xml
       //movie[count(cast/actor) > 5]
```
  c)      Получить все фильмы, в которых указанный человек (задается в запросе константой) является и режиссером и актором одновременно. Например, "Christopher Nolan")
```xml
       //movie[directors/director="Christopher Nolan" and cast/actor="Christopher Nolan"]
```
 d)      Сформировать список просмотра из заданного количества фильмов указанного жанра. Порядок фильмов определяется случайным образом. Например, 3 фильма жанра "Drama"
 ```xml
       //movie[genres/genre="Drama"][position() <= 3]
```
 e)      Собственный запрос с использование минимум двух функций count(), contains(), position(), sum() и др. Получить общее количество актеров в фильмах с кассовыми сборами выше 500 млн и вывести все названия фильмов, в которых участвует актер с именем "Leonardo DiCaprio":
  ```xml
       sum(//movie[box_office > 500000000]/count(cast/actor))
       //movie[cast/actor="Leonardo DiCaprio"]/title
```
3.  Описать DTD схему для разработанного формата. Произвести валидацию xml-документа (0,5 балла). Валидация в вижуалке
```xml
<!DOCTYPE movies [
    <!ELEMENT movies (movie+)>
    <!ELEMENT movie (title, genres, directors, composers, cast, release_date, box_office, age_rating, audience_count, original_language)>
    
    <!ELEMENT title (#PCDATA)>
    <!ELEMENT genres (genre+)>
    <!ELEMENT genre (#PCDATA)>
    
    <!ELEMENT directors (director+)>
    <!ELEMENT director (#PCDATA)>
    
    <!ELEMENT composers (composer+)>
    <!ELEMENT composer (#PCDATA)>
    
    <!ELEMENT cast (actor+)>
    <!ELEMENT actor (#PCDATA)>
    
    <!ELEMENT release_date (#PCDATA)>
    <!ELEMENT box_office (#PCDATA)>
    <!ELEMENT age_rating (#PCDATA)>
    <!ELEMENT audience_count (#PCDATA)>
    <!ELEMENT original_language (#PCDATA)>
]>
```
 - Описание DTD-схемы:
    - <!ELEMENT movies (movie+)> — определяет, что корневой элемент <movies> содержит один или более элементов <movie>.
    - <!ELEMENT movie (...)> — описывает структуру элемента <movie>, указывая, что он состоит из обязательных элементов: <title>, <genres>, <directors>, <composers>, <cast>, <release_date>, <box_office>, <age_rating>, <audience_count>, и <original_language>.
    - <!ELEMENT genres (genre+)> — указывает, что элемент <genres> содержит один или несколько <genre>.
    - Аналогично для directors, composers и cast: каждый из этих элементов может содержать один или более соответствующих элементов (например, <director>, <composer>, <actor>).
    - Все элементы, содержащие только текстовые данные, определяются как #PCDATA.
4.       Описать XML Schema для разработанного формата. Произвести валидацию xml-документа. (0,5 балл). Валидация в вижуалке. Новая схема = схема, созданная на основе XML, а старая схема - схема, созданная с использованием DTD
      
Ключевые различия между схемами:
     a) Типы данных для числовых и датированных элементов: В новой схеме используются более строгие типы (Это делает схему более строгой и подходящей для проверки данных):
     -  release_date: xs:date вместо xs:string.
     - box_office и audience_count: xs:unsignedInt вместо xs:string.        
     b) Количество режиссеров:              
     -  В новой схеме элемент <directors> может содержать только одного <director>.
     - В старой схеме можно было указать несколько режиссеров.
     c). Использование maxOccurs:
     - В новой схеме многие элементы (например, <genre>, <composer>, <actor>) явно имеют атрибут maxOccurs="unbounded", что делает правила повторяемости более строгими.
     - В старой схеме повторяемость определялась в отдельных элементах (например, через ссылку ref).
     d). Упрощение структуры:
     - В новой схеме элементы напрямую определяются внутри <movie> (например, <genre>), вместо использования ссылок (ref) на внешние определения, как это было в старой схеме.
     
5.   Описать XSLT-преобразование xml-документа в текстовый вид (*.txt). (1 балл)
      https://www.freeformatter.com/xsl-transformer.html#before-output

6. Описать XSLT-преобразование xml-документа в html-страницу (информация должна быть представлено в табличном виде), при оформлении таблицы использованы стили (1 балл)
https://html.onlineviewer.net/
Берем XML:
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
Берем HSLT:
```xml
<?xml version="1.0" encoding="UTF-8"?>
<xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform">
    <xsl:output method="html" encoding="UTF-8"/>
    
    <xsl:template match="/movies">
        <html>
            <head>
                <style>
                    table {
                        font-family: Arial, sans-serif;
                        border-collapse: collapse;
                        width: 100%;
                    }
                    th, td {
                        border: 1px solid #dddddd;
                        text-align: left;
                        padding: 8px;
                    }
                    th {
                        background-color: #f2f2f2;
                    }
                </style>
                <title>Movie Collection</title>
            </head>
            <body>
                <h2>Movie Collection</h2>
                <table>
                    <tr>
                        <th>Title</th>
                        <th>Genres</th>
                        <th>Director(s)</th>
                        <th>Composer(s)</th>
                        <th>Cast</th>
                        <th>Release Date</th>
                        <th>Box Office</th>
                        <th>Age Rating</th>
                        <th>Audience Count</th>
                        <th>Language</th>
                    </tr>
                    <xsl:for-each select="movie">
                        <tr>
                            <td><xsl:value-of select="title"/></td>
                            <td>
                                <xsl:for-each select="genres/genre">
                                    <xsl:value-of select="."/><xsl:if test="position() != last()">, </xsl:if>
                                </xsl:for-each>
                            </td>
                            <td>
                                <xsl:for-each select="directors/director">
                                    <xsl:value-of select="."/><xsl:if test="position() != last()">, </xsl:if>
                                </xsl:for-each>
                            </td>
                            <td>
                                <xsl:for-each select="composers/composer">
                                    <xsl:value-of select="."/><xsl:if test="position() != last()">, </xsl:if>
                                </xsl:for-each>
                            </td>
                            <td>
                                <xsl:for-each select="cast/actor">
                                    <xsl:value-of select="."/><xsl:if test="position() != last()">, </xsl:if>
                                </xsl:for-each>
                            </td>
                            <td><xsl:value-of select="release_date"/></td>
                            <td><xsl:value-of select="box_office"/></td>
                            <td><xsl:value-of select="age_rating"/></td>
                            <td><xsl:value-of select="audience_count"/></td>
                            <td><xsl:value-of select="original_language"/></td>
                        </tr>
                    </xsl:for-each>
                </table>
            </body>
        </html>
    </xsl:template>
</xsl:stylesheet>
```
Итог HML страница:
```xml
<html>
   <head>
      <style>
                    table {
                        font-family: Arial, sans-serif;
                        border-collapse: collapse;
                        width: 100%;
                    }
                    th, td {
                        border: 1px solid #dddddd;
                        text-align: left;
                        padding: 8px;
                    }
                    th {
                        background-color: #f2f2f2;
                    }
                </style>
      <title>Movie Collection</title>
   </head>
   <body>
      <h2>Movie Collection</h2>
      <table>
         <tr>
            <th>Title</th>
            <th>Genres</th>
            <th>Director(s)</th>
            <th>Composer(s)</th>
            <th>Cast</th>
            <th>Release Date</th>
            <th>Box Office</th>
            <th>Age Rating</th>
            <th>Audience Count</th>
            <th>Language</th>
         </tr>
         <tr>
            <td>Inception</td>
            <td>Sci-Fi, Thriller</td>
            <td>Christopher Nolan</td>
            <td>Hans Zimmer</td>
            <td>Leonardo DiCaprio, Joseph Gordon-Levitt, Ellen Page, Tom Hardy, Ken Watanabe, Cillian Murphy</td>
            <td>2010-07-16</td>
            <td>829895144</td>
            <td>PG-13</td>
            <td>10000000</td>
            <td>English</td>
         </tr>
         <tr>
            <td>Interstellar</td>
            <td>Sci-Fi, Drama</td>
            <td>Christopher Nolan</td>
            <td>Hans Zimmer</td>
            <td>Matthew McConaughey, Anne Hathaway, Jessica Chastain, Michael Caine, Casey Affleck</td>
            <td>2014-11-07</td>
            <td>677471339</td>
            <td>PG-13</td>
            <td>8000000</td>
            <td>English</td>
         </tr>
         <tr>
            <td>Pulp Fiction</td>
            <td>Crime, Drama</td>
            <td>Quentin Tarantino</td>
            <td>Various</td>
            <td>John Travolta, Uma Thurman, Samuel L. Jackson, Bruce Willis</td>
            <td>1994-10-14</td>
            <td>213928762</td>
            <td>R</td>
            <td>5000000</td>
            <td>English</td>
         </tr>
         <tr>
            <td>The Dark Knight</td>
            <td>Action, Crime</td>
            <td>Christopher Nolan</td>
            <td>Hans Zimmer, James Newton Howard</td>
            <td>Christian Bale, Heath Ledger, Aaron Eckhart, Michael Caine, Maggie Gyllenhaal</td>
            <td>2008-07-18</td>
            <td>1004558444</td>
            <td>PG-13</td>
            <td>12000000</td>
            <td>English</td>
         </tr>
         <tr>
            <td>The Grand Budapest Hotel</td>
            <td>Comedy, Drama</td>
            <td>Wes Anderson</td>
            <td>Alexandre Desplat</td>
            <td>Ralph Fiennes, Tony Revolori, F. Murray Abraham, Adrien Brody, Willem Dafoe</td>
            <td>2014-03-28</td>
            <td>174600318</td>
            <td>R</td>
            <td>3000000</td>
            <td>English</td>
         </tr>
      </table>
   </body>
</html>
```
8. Разработать программу на любом языке программирования (Python, С#, Java) для выполнения XSLT- преобразования и разработанных xPath-запросов. (2 балл)
https://colab.research.google.com/drive/1ww688bPLzIk8BcVRQDnduy2bqIo7XXlq?hl=ru#scrollTo=haFz0bcKiHxu

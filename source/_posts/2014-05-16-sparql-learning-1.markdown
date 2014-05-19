*Recently, I'm studing about SPARQL. And I have read many pretty good blogs or article, thus, it's neccessary to record those things here. Meanwhile, this contains how I understand SPARQL.*

<text style="font-weight:bold; font-size:20px">KEYWORDS</text>&nbsp;&nbsp;&nbsp;&nbsp;SPARQL Queries&nbsp;&nbsp;&nbsp;&nbsp;GRAPH&nbsp;&nbsp;&nbsp;&nbsp;

#(I) Queries#
(1). The basic query, s means subject, p means predicate and o means object.

```
SELECT * 
WHERE
{
	?s ?p ?o
}
```


(2). A table of some keywords. It will up-to-date.


| Keywords  | Description               |
| ------------------------- | :-----------------------: |
| OPTIONAL  | If we have some options.  |
| NOT EXIST | If not exist, return true. Otherwise, return false.|
| MINUS     | In most time, same as NOT EXIST.|
| DISTINCT  | Get rid of those duplicate results.|
| UNION     | Search for multi-graph of multi-rdf.|
| FILTER    | It just has one arguement and the return value must be boolean.|
| IN        | To enumerate data.|
| LIMIT     | To limit the number of data which we get. |
| OFFSET    | To skip some results. |
| ^         | Reverse. |

#(II) Graph#

*In this section, I understand graph by learning keywords **FROM** and **FROM NAMED**.

```
SELECT *
  …FROM or FROM NAMED dataset specifiers …
{
	{?s?p?o}
	UNION
	{GRAPH ?g{?s?p?o}}
}
```

&nbsp;&nbsp;&nbsp;&nbsp;(a)**FROM** builds only the default graph.

&nbsp;&nbsp;&nbsp;&nbsp;(b)**FROM NAMED** builds only the named graphs.

&nbsp;&nbsp;&nbsp;&nbsp;Like the psudo-code above, the portion GRAPH ?g{?s?p?o} means query all unnamed graphs. Thus, the code means get all triples in both the unnamed graph and named graphs.

<br></br>
###Reference###
1. [Defining the Semantic Graph - What is it Really? ](http://www.novaspivack.com/web-3-0/defining-the-semantic-graph-what-is-it-really)
2. [A Narrative for Understanding SPARQL's: FROM, FROM NAMED and GRAPH](http://yarcdata.com/blog/?p=201)
3. [The Friend of a Friend (FOAF) project](http://www.foaf-project.org/)
4. [How Semantic Search is Killing the Keyword](http://www.imediaconnection.com/content/35588.asp)







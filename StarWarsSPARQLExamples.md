# My Star Wars Ontology: SPARQL Examples
## Where is the homeworld of Luke Skywalker?
```ttl
# Where is the homeworld of Luke Skywalker?
PREFIX : <http://mystarwarsontology-graph.com/>
SELECT ?h
WHERE {
	:Luke_Skywalker :homeworld ?h
}
```
## What are the episodes that Luke appears in?
```ttl
# What are the episodes that Luke appears in?
PREFIX : <http://mystarwarsontology-graph.com/>
SELECT ?e ?fName
WHERE {
	:Luke_Skywalker :appears_in ?f .
	?f :name ?fName ;
	   :episode ?e
} ORDER BY ASC (?e)
```
## What are the release dates of the Films?
```ttl
# What are the release dates of the Films?
PREFIX : <http://mystarwarsontology-graph.com/>
SELECT ?f ?e ?date
WHERE {
	?f a :Film ;
		:episode ?e ;
		:release_date ?date 
} ORDER BY ASC (?date)
```
## List the characters who appears in 2 films
```ttl
# List the characters who appears in 2 films
PREFIX : <http://mystarwarsontology-graph.com/>
SELECT DISTINCT ?c 
WHERE {
  ?c :appears_in ?f1 , ?f2 .
  FILTER(?f1 != ?f2)
}
```
## List the characters who appears in both ep.1 and sequels.
```ttl
# List the characters who appears in both ep.1 and sequels.
PREFIX : <http://mystarwarsontology-graph.com/>
SELECT DISTINCT ?c 
WHERE {
  ?c :appears_in ?f1 , ?f2 .
  ?f1 :episode ?e1 .
  ?f2 :episode ?e2 .
  FILTER(?e1 = 1 && ?e2 IN (7, 8, 9))
}
```

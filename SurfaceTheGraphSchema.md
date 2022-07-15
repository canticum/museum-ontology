# Use SPARQL query to surface the graph schema
## 1. What are the types of things that are in the graph?
```ttl
# What are the types of things that are in the graph?
SELECT DISTINCT ?t
WHERE {
	?s a ?t
}
GROUP BY ?t
ORDER BY ASC(?t)
```
## 2. What are the predicates defined in the graph?
```ttl
# What are the predicates defined in the graph?
SELECT DISTINCT ?p
WHERE {
	?s ?p ?o
}
ORDER BY ASC(?p)
```
## 3. What is the full vocabulary for the graph?
```ttl
# What is the full vocabulary for the graph?
SELECT DISTINCT ?t ?p
WHERE {
	?s ?p ?o ;
		a ?t
}
GROUP BY ?t ?p
ORDER BY ASC(?t) ASC(?p)
```
## 4. What is the full vocabulary for the graph?
```ttl
# What is the full vocabulary for the graph?
SELECT DISTINCT ?t ?p ?pType
WHERE {
	?s ?p ?o ;
		a ?t
BIND( COALESCE(
		IF(isIRI(?o), "Resource Predicate", 1/0),
		"Literal Predicate") AS ?pType)
}
GROUP BY ?t ?p ?pType
ORDER BY ASC(?t) ASC(?p)
```

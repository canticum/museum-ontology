# My Star Wars Ontology
```ttl
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX : <http://mystarwarsontology-graph.com/>

  # Luke Skywalker
  :Luke_Skywalker a :Star_Wars_Character ;
          :name "Luke Skywalker" ;
          :gender "Male" ;
          :species "Human" ;
          :homeworld :Tatooine ;
          :force_sensitive true ;
          :appears_in :Revenge_of_the_Sith , :A_New_Hope , 
                      :The_Empire_Strikes_Back , :Return_of_the_Jedi .

  # Leia Organa
  :Leia_Organa a :Star_Wars_Character ;
      :name "Leia Organa" ;
      :gender "Female" ;
      :species "Human" ;
      :homeworld :Alderaan ;
      :force_sensitive true ;
      :appears_in :Revenge_of_the_Sith , :A_New_Hope ,
                  :The_Empire_Strikes_Back , :Return_of_the_Jedi .

  # Chewbacca
  :Chewbacca a :Star_Wars_Character ;
      :name "Chewbacca" ;
      :gender "Male" ;
      :species "Wookiee" ;
      :homeworld :Kashyyyk ;
      :nickname "Chewie" ;
	  :force_sensitive false ;
      :appears_in :Revenge_of_the_Sith , :A_New_Hope ,
                  :The_Empire_Strikes_Back , :Return_of_the_Jedi .

  # R2-D2
  :R2_D2 a :Star_Wars_Character ;
      :name "R2-D2" ;
      :species "Droid" ;
      :homeworld :Naboo ;
      :nickname "Artoo" ;
      :gender "Masculine Programming" ;
	  :force_sensitive false ;
      :appears_in :The_Phantom_Menace , :Attack_of_the_Clones ,
                  :Revenge_of_the_Sith , :A_New_Hope ,
                  :The_Empire_Strikes_Back , :Return_of_the_Jedi .

  #Tatooine
  :Tatooine a :Planet ;
      :name "Tatooine" .

  #Alderaan
  :Alderaan a :Planet ;
      :name "Alderaan" .

  #Kashyyyk
  :Kashyyyk a :Planet ;
      :name "Kashyyyk" .

  #Naboo
  :Naboo a :Planet ;
      :name "Naboo" .

  # The Phantom Menace (episode 1)
  :The_Phantom_Menace a :Film ;
          :name "The Phantom Menace" ;
          :release_date "1999-05-19"^^xsd:date ;
          :episode 1 .

  # Attack of the Clones (episode 2)
  :Attack_of_the_Clones a :Film ;
          :name "Attack of the Clones" ;
          :release_date "2002-05-16"^^xsd:date ;
          :episode 2 .

  # Revenge of the Sith (episode 3)
  :Revenge_of_the_Sith a :Film ;
          :name "Revenge of the Sith" ;
          :release_date "2005-05-15"^^xsd:date ;
          :episode 3 .

  # A New Hope (episode 4)
  :A_New_Hope a :Film ;
          :name "A New Hope" ;
          :release_date "1977-05-25"^^xsd:date ;
          :episode 4 .

  # The Empire Strikes Back (episode 5)
  :The_Empire_Strikes_Back a :Film ;
          :name "The Empire Strikes Back" ;
          :release_date "1980-05-17"^^xsd:date ;
          :episode 5 .

  # Return of the Jedi (episode 6)
  :Return_of_the_Jedi a :Film ;
          :name "Return of the Jedi" ;
          :release_date "1983-05-25"^^xsd:date ;
          :episode 6 .
          
  # The Force Awakens (episode 7)
  :The_Force_Awakens a :Film ;
          :name "The Force Awakens" ;
          :release_date "2015-12-14"^^xsd:date ;
          :episode 7 .

  # The Last Jedi (episode 8)
  :The_Last_Jedi a :Film ;
          :name "The Last Jedi" ;
          :release_date "2017-12-09"^^xsd:date ;
          :episode 8 .

  # The Rise of Skywalker (episode 9)
  :The_Rise_of_Skywalker a :Film ;
          :name "The Rise of Skywalker" ;
          :release_date "2019-12-16"^^xsd:date ;
          :episode 9 .
          
  :Luke_Skywalker :appears_in :The_Force_Awakens , :The_Last_Jedi , :The_Rise_of_Skywalker .

  :Leia_Organa :appears_in :The_Force_Awakens , :The_Last_Jedi , :The_Rise_of_Skywalker .

  :Chewbacca :appears_in :The_Force_Awakens , :The_Last_Jedi , :The_Rise_of_Skywalker .

  :R2_D2 :appears_in :The_Force_Awakens , :The_Last_Jedi , :The_Rise_of_Skywalker .
          
  # Mark Hamill
  :Luke_Skywalker :portrayed_by :Mark_Hamill .
  :Mark_Hamill a :Person ;
      :name "Mark Richard Hamill" ;
      :gender "Male" ;
      :born_on "1951-09-25"^^xsd:date .

  # Carrie Fisher
  :Leia_Organa :portrayed_by :Carrie_Fisher .
  :Carrie_Fisher a :Person ;
      :name "Carrie Frances Fisher" ;
      :gender "Female" ;
      :born_on "1956-10-21"^^xsd:date ;
      :died_on "2016-12-27"^^xsd:date .

  # Deep Roy
  :R2_D2 :played_by :Deep_Roy .
  :Deep_Roy a :Person ;
      :name "Gurdeep Roy" ;
      :gender "Male" ;
      :born_on "1949-01-26"^^xsd:date .

  # Kenny Baker
  :R2_D2 :played_by :Kenny_Baker .
  :Kenny_Baker a :Person ;
      :name "Kenneth George Baker" ;
      :gender "Male" ;
      :born_on "1934-08-24"^^xsd:date ;
      :died_on "2016-08-13"^^xsd:date .

  # Jimmy Vee
  :R2_D2 :played_by :Jimmy_Vee .
  :Jimmy_Vee a :Person ;
      :name "James Vee" ;
      :gender "Male" ;
      :born_on "1959-02-03"^^xsd:date .

  # Peter Mayhew
  :Chewbacca :played_by :Peter_Mayhew .
  :Peter_Mayhew a :Person ;
      :name "Peter William Mayhew" ;
      :gender "Male" ;
      :born_on "1944-05-19"^^xsd:date ;
      :died_on "2019-04-30"^^xsd:date .

  # Joonas Suotamo
  :Chewbacca :played_by :Joonas_Suotamo .
  :Joonas_Suotamo a :Person ;
      :name "Joonas Vijami Suotamo" ;
      :gender "Male" ;
      :born_on "1986-10-03"^^xsd:date .

  # Ben Burtt
  :R2_D2 :voiced_by :Ben_Burtt .
  :Chewbacca :voiced_by :Ben_Burtt .
  :Ben_Burtt a :Person ;
      :name "Benjamin Burtt Jr." ;
      :gender "Male" ;
      :born_on "1948-07-12"^^xsd:date .
```

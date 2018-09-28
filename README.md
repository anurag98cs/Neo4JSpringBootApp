"# Neo4JSpringBootApp" 

Cypher query to create data into Neo4J
--------------------------------------------------------------------------------

CREATE (Inception:Movie {title: 'Inception', director: 'Christopher Nolan'})
CREATE (DarkKnight:Movie {title: 'The Dark Knight', director: 'Christopher Nolan'})
CREATE (Peter:User {name: 'Peter N', age: 30})
CREATE (Sam:User {name: 'Sam Sheldon', age: 28})
CREATE (Ryan:User {name: 'Ryan A', age: 35})

CREATE 
(Inception)-[:RATED {rating: 9}]->(Peter),
(Inception)-[:RATED {rating: 8}]->(Sam),
(DarkKnight)-[:RATED {rating: 8}]->(Peter),
(DarkKnight)-[:RATED {rating: 9}]->(Sam);

-------------------------------------------------------------------------------


To run the Neo4J Docker image 
---------------------------------
Docker Shell>docker run     --publish=7474:7474 --publish=7687:7687     --volume=$HOME/neo4j/data:/data     --volume=$HOME/neo4j/l
ogs:/logs     neo4j

To stop all the containers
---------------------------------
Docker Shell>docker stop $(docker ps -a -q)

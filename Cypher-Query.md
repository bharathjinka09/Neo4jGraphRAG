CREATE(Nolan:Person{name:"Christopher Nolan", born:1970})

CREATE(Leo:Person{name:"Leonardo DiCaprio", born:1974})

CREATE(Matthew:Person{name:"Matthew McConaughey", born:1969})


CREATE(Inception:Movie{title:"Inception", released:2010})

CREATE(Interstellar:Movie{title:"Interstellar", released:2014})


MATCH (Nolan:Person {name: "Christopher Nolan"}),
      (Inception:Movie {title: "Inception"})
CREATE (Nolan)-[:DIRECTED]->(Inception);


MATCH (Nolan:Person {name: "Christopher Nolan"}),
      (Interstellar:Movie {title: "Interstellar"})
CREATE (Nolan)-[:DIRECTED]->(Interstellar);


MATCH (Leo:Person {name: "Leonardo DiCaprio"}),
      (Inception:Movie {title: "Inception"})
CREATE (Leo)-[:ACTED_IN]->(Inception);


MATCH (Matthew:Person {name: "Matthew McConaughey"}),
      (Interstellar:Movie {title: "Interstellar"})
CREATE (Matthew)-[:ACTED_IN]->(Interstellar);

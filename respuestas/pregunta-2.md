MATCH (p:Persona)-[:VIVE_EN]->(c:Ciudad {nombre: "Madrid"})
RETURN p.nombre
LIMIT 2
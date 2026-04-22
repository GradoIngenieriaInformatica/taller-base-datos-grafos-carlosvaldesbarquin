MATCH (p:Persona)-[:AMIGO_DE]->(amigo:Persona)-[:VIVE_EN]->(c:Ciudad)
RETURN p.nombre AS persona, collect(DISTINCT c.nombre) AS ciudades_amigos
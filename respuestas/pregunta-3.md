MATCH (p:Persona)-[rel:PARTICIPA_EN]->(pr:Proyecto)
RETURN pr.nombre AS proyecto, sum(rel.horas) AS total_horas
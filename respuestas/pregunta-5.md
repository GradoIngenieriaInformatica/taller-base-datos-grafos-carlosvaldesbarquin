MATCH (p:Persona)-[:AMIGO_DE*2..]->(indirecto:Persona)
WHERE p <> indirecto AND NOT (p)-[:AMIGO_DE]->(indirecto)
WITH p, count(DISTINCT indirecto) AS conexiones_indirectas
ORDER BY conexiones_indirectas DESC
LIMIT 1
RETURN p.nombre AS persona, conexiones_indirectas
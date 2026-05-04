# Day 13 — Analyse SQL d'un Music Store Digital

## Objectif

Analyser la base de données d'un magasin de musique digital
pour répondre à des questions business concrètes,
en progressant de requêtes simples vers des requêtes avancées.

## Dataset

Base de données relationnelle — 11 tables interconnectées :
`employee`, `customer`, `invoice`, `invoice_line`,
`track`, `album`, `artist`, `genre`, `media_type`,
`playlist`, `playlist_track`

## Stack technique

- PostgreSQL
- PgAdmin4

## Structure des questions

### Niveau 1 — Easy
- Employé le plus senior (ORDER BY levels)
- Pays avec le plus de factures (GROUP BY + COUNT)
- Top 3 des factures (ORDER BY total DESC)
- Ville avec le plus fort CA (SUM + GROUP BY)
- Meilleur client global (JOIN + SUM)

### Niveau 2 — Moderate
- Auditeurs Rock : email + prénom + nom (JOIN multi-tables + WHERE subquery)
- Top 10 artistes Rock par nombre de tracks (JOIN + GROUP BY + COUNT)
- Tracks au-dessus de la durée moyenne (Subquery + AVG)

### Niveau 3 — Advanced
- Dépense par client et par artiste (CTE + multi-JOIN)
- Genre le plus populaire par pays (CTE + ROW_NUMBER Window Function)
- Top client par pays avec gestion des ex-aequo (CTE + PARTITION BY)

## Concepts clés abordés

| Concept | Usage |
|---|---|
| `JOIN` multi-tables | Traverser 4-5 tables pour une réponse |
| Subquery | Filtrer dynamiquement sur un résultat calculé |
| `GROUP BY` + agrégats | Consolider les données par dimension |
| CTE (`WITH`) | Structurer les requêtes complexes |
| Window Function `ROW_NUMBER() OVER(PARTITION BY)` | Classement par groupe |

## Schéma de la base

![Music Database Schema](MusicDatabaseSchema.png)

## Fichiers

| Fichier | Description |
|---|---|
| `Music_Store_Query.sql` | Toutes les requêtes du projet |
| `Music_Store_database.sql` | Script de création de la base |
| `MusicDatabaseSchema.png` | Schéma relationnel |

## Projet original

Inspiré du tutoriel de [Rishabh Mishra](https://www.youtube.com/@RishabhMishraOfficial)

---

*Day 13 / 30 — #30DaysChallenge #SQL #DataEngineering #BuildInPublic*

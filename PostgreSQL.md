# PostgreSQL

## Nils Skulte DP4-4

---

## Kas ir PostgreSQL

PostgreSQL ir datubāžu vadības sistēma, kas ir bāzēta uz SQL valodas.  
Tā ir ļoti viegli pieejama, ir ļoti uzticama un uztur tavus datus.

---

## Windows instalācija

1. Lejupielādē PostgreSQL instalātoru no [PostgreSQL Downloads](https://www.postgresql.org/download/).
2. Uzstādi to atkarībā no tavām nepieciešamībām.
3. Lai pārbaudītu, vai PostgreSQL strādā:
   - Aizej uz Start -> Run -> Services.msc.
   - Sameklē «postgresql-[versija]» servisu.
### Ja tu redzi PostgreSQL servisu, tas strādā 

---

## Testēšana

# Atver komandrindu un ievadi:

    psql -U postgres

## (tev prasīs paroli, tālāk tiksi pēc ievadīšanas).
---
# Kad esi savienojies ar PostgreSQL, izveido datubāzi ar nosaukumu "testdb":

    CREATE DATABASE testdb;
---
# Izvēlies testdb:

    \c testdb
---
# Izveido kkādu tabulu:

    CREATE TABLE example (
    id SERIAL PRIMARY KEY,
    name VARCHAR(50)
    );
---
# Ieraksti ierakstu:

    INSERT INTO example (name) VALUES ('Tests');
---
# Apskati ierakstus:

    SELECT * FROM example;
---
# Ja uzrādās tabula ar vienu ierakstu ar nosaukumu "Tests", PostgreSQL strādā.

--- 
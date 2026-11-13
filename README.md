# jazztimeline-data

Open, cited data on jazz recordings, personnel and apprenticeship lineage.

This is the dataset behind JazzTimeline, a research instrument for studying the people, places and teaching lines behind the music, built so that every claim carries its source.

## Status

Early. The schema is still moving. Nothing here is stable enough to build on yet.

## What will be here

| File | Holds |
| --- | --- |
| people.json | Musicians: names, instruments, dates, birthplace, gender where stated |
| sessions.json | Recording sessions: date, label, studio, city, credited personnel |
| ensembles.json | Ensembles treated as apprenticeship schools, with membership and dates |
| relationships.json | Teaching and mentorship edges between people |
| sources.json | The source registry, with a tier for each source |
| schema/ | Field definitions, controlled vocabularies, and a validator |

## How sources are handled

Every claim records where it came from, and every source carries a tier.

| Tier | Meaning | Examples |
| --- | --- | --- |
| A | Institutional authority | DAHR, Library of Congress, published discographies |
| B | Scholarly secondary | Peer-reviewed work, university press, Linked Jazz |
| C | Community aggregate | MusicBrainz, Wikidata, Discogs |
| D | Self-reported | Interview or memoir |

Tier C is a lead, not a citation. It is used to find a fact quickly, then upgraded to A or B before anything rests on it.

Two rules we hold to:

- Nothing is inferred. A fact is recorded because a source states it.
- No false negatives. Absence from a discography is missing data, not evidence of absence. Coverage is expressed as no session in this corpus, never as never.

## Relationship types

Four, kept distinct on purpose:

- Formal study: enrolled or private instruction with a named teacher
- Bandstand apprenticeship: hired into an ensemble that functioned as a school
- Informal mentorship: guidance outside employment
- Acknowledged influence: one-directional, stated by the musician, never merged with the three above

Every edge carries direction, years, nature, sources and a confidence flag.

## Licences

Two, deliberately. Factual data is CC0; editorial content is CC BY 4.0. See LICENSES.md.

## Contributing

Not open yet. When it is, the entry rules will live in schema/.

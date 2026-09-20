# site-energy
Behind the meter and embedded generation of electricity where grid may be limited and or energy costs high

## Saved simulations (first seed, 20 September 2026)

2293 saved simulations of generic sites behind the meter. None is a real site: sizes are round, typical figures, and every
electrical figure is marked as an estimate that an owner overwrites with their own. Each record holds the question in plain
words, the **pop command** that reruns it with every input inside it, the numbers, what was assumed, and a verdict that could
have been REFUTED.

| family | what it asks | records |
|---|---|---|
| SITE PULSE | an industrial site with its own intake, several site transformers, solar on one low voltage board, a generator and an export limit: what flows at the connection point, what each bus sees, how loaded each transformer is | 24 |
| SITE THRESHOLDS | how much solar before the export limit, the voltage band or a transformer rating binds (found by halving) | 3 |
| SITE SURVEY | two thousand generated sites in the hard case (full solar, light load): how often each limit binds | 2000 |
| SITE ENERGY | a very large private network hour by hour for a year: how much of its own electricity it makes for a given solar and battery size | 31 |
| DC TRACTION | solar fed on the direct current side of a metro's traction system against the usual route | 18 |
| CABLE CHECK | the four questions of a cable sizing study: current, voltage drop, fault withstand, and when to commission a thermal study | 217 |

- `records/ledger.jsonl` : one line a record. `index.html` : every record as a dot; tap one to read it and its pop command.
- The code that produced them, and the runner that reruns them, live in [Ventusltd/faraday](https://github.com/Ventusltd/faraday) under `bench/` (`python bench/one.py N` reruns record N). One copy of the code, there; the records for this subject, here.
- What the survey found: on generated sites the export limit and the transformer beside the solar bind long before voltage does.

Estimates from stated generic figures, to decide which engineering study is worth commissioning. Not a design, not a study, not a connection offer. Provided as is, without warranty of any kind. Above 100 kW a chartered electrical engineer must sign the real thing.

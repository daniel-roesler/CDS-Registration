# CDS WG1 (Registration) Meeting 2026-08-06

Recording: https://zoom.us/rec/share/mxNf3a0moEfLktmkIvwjK7VOqEku-sGuMIXLbAzeOndHnbn7yZwA-R5_TNNqMltr.sq8MOoqwsCwtaLe2

## Agenda
* Welcome
* Review new experimental OpenAPI / Swagger interface for CDS-WG1-01 schema
    * Issue: https://github.com/lfe-cds/CDS-Registration/issues/12
    * Preview: https://daniel-roesler.github.io/CDS-Registration/specs/cds-wg1-01/openapi

## Attendees
* Daniel Roesler (Maintainer)
* Blade Chapman (Apple)
* Don Coffin (GBA)

## Minutes
* Welcome and intros
* Showing experimental Swagger interface on maintainer branch
* Discussed architecture in the repo

```
cds-registration.lfenergy.org/openapi?spec=cds-wg1-01
```

* TODO: Explore authentication interface for "Try it out" using the demo server

* Add technical/development tab at the top of the website
    * "Examples"? "Docs"? "Code"? "Dev Examples"?
    * Put both OpenAPI interface + curl examples in this section
    * Not really a need anymore for SDKs (since agents can build those on demand)
    * Though maybe multi-language examples in addition to curl?


## Closing Discussion
* Consensus to commit this to repo? Yes

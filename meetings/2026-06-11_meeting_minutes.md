# CDS WG1 (Registration) Meeting 2026-06-11

Recording: https://zoom.us/rec/share/yfc20q1Z5g4UUytc0d362Lqwhce0DTiZjzCCoO-_HnNFrq7aM8fGGBr0ytKULpg2.LBkyHhTX3-Ro-YYd

## Agenda
* Welcome
* New issue and pull request (adding `entity_number` to Coverage Entry objects)
    * Issue: https://github.com/lfe-cds/CDS-Registration/issues/21
    * Pull Request: https://github.com/lfe-cds/CDS-Registration/pull/22
* Previous issue and pull request (adding additional formats to registration and authorization details fields)
    * Issue: https://github.com/lfe-cds/CDS-Registration/issues/15
    * Pull Request: https://github.com/lfe-cds/CDS-Registration/pull/16
* Previous issue and pull request (associating Grant objects with authorization/token requests)
    * Issue: https://github.com/lfe-cds/CDS-Registration/issues/18
    * Pull Request: https://github.com/lfe-cds/CDS-Registration/pull/20

## Attendees
* Daniel Roesler (Maintainer)
* Don Coffin (GBA)

## Minutes
* Review https://github.com/lfe-cds/CDS-Registration/issues/21
* Discuss https://github.com/lfe-cds/CDS-Registration/issues/19
* Discuss https://github.com/lfe-cds/CDS-Registration/issues/18

```
POST /register
{
    "client_name": "ABC Company",
    "scope": "cds_client_admin cds_customer_data",
    ...
}

Response:
{
    "client_id": "aaaaaa",
    "client_secret": "bbbbbbb",
    "scope": "cds_client_admin",
    ...
}
(then on the Client API, there will be another Client Object that's for the scope: "cds_customer_data")



POST /oauth/token
Authorization: Basic b64({client_id}:{client_secret})
{
    "grant_type: "client_credentials",
}
Response:
{
    "access_token": "cccccccccc",
    ...
}

GET /cds-api/clients
Authorization: Bearer cccccccccc
{
    "clients": [
        {
            "client_id": "49949494949",
            "scope": "cds_customer_data",
            ...
        },
        ...
    ],
    ...
}
```


## Closing Discussion
* Consensus to commit this to repo? Yes


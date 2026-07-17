# API Use Cases

An API Use Case is a machine-readable description of how an API is actually meant to be put to work—capturing who is using the API, what they are doing with it, how, why, and where, and tying that story down to the specific OpenAPI operations involved. Use cases align the business and technical sides of the API conversation, making sure that the reasons an API exists stay connected to the endpoints that deliver on them. They are one of the most useful building blocks for keeping producers focused on real consumer value across the API lifecycle.

## API Commons

An API Use Case is an [API Commons](http://apicommons.org) building block—an open, machine-readable schema that can be used as a common property, or as an individual API property, within an APIs.json. It is indexed as a `Common` type within its [APIs.json](apis.yml) index, letting it be discovered, referenced, and reused across the APIs.json ecosystem and surfaced through [apis.io](https://apis.io). This schema is just getting started, and the process and the schema will mature as it is applied across more APIs.

## What's in this repo

- [use-case-schema.yml](use-case-schema.yml) — The JSON Schema that defines a use case.
- [use-case-example.yml](use-case-example.yml) — A worked example describing a single use case.
- [apis.yml](apis.yml) — The APIs.json index for this building block, referencing the schema and example as `Common` artifacts.

## The Schema

The [use-case-schema.yml](use-case-schema.yml) defines each use case as an object with the following properties:

- **who** — Who (person or demographic) is using an API, focusing on the person, team, company, or demographic behind usage.
- **what** — What the consumer is going to do with the API, focusing on the big picture of the application or integration.
- **how** — How a consumer is going to use an API, focusing on the technical details of programming language or integration.
- **why** — Why the consumer is going to use an API, getting at the incentive that motivates a consumer.
- **where** — Where the API will be used by the consumer—on-premise, in the cloud, and other geographical or regional details.
- **operations** — An array of the unique OpenAPI `operationId` values that apply to this use case, ensuring technical alignment.

## Example

The [use-case-example.yml](use-case-example.yml) file describes a single use case:

```yaml
who: APIs.io Website Developer
what: Open-Source API Search Engine
how: Client-Side Javascript Calls
why: Power the Network Websites
where: Static GitHub Pages Websites
description: This is the initial and primary use case for APIs.io website...
operations:
  - searchAPIs
  - addAPIs
```

## How It Fits

Use cases are one of a growing set of API Commons building blocks that describe the business and technical realities of API operations in a machine-readable way. Because a use case references OpenAPI `operationId` values, it forms a direct bridge between the business story and the technical contract. It cross-links with the [change log](https://github.com/api-commons/change-log), [road map](https://github.com/api-commons/road-map), [teams](https://github.com/api-commons/teams), [plans](https://github.com/api-commons/plans), [guidance](https://github.com/api-commons/guidance), [policies](https://github.com/api-commons/policies), and other building blocks—each a small, reusable schema that can stand alone or be composed together within an APIs.json index.

## Support

This work is in an early stage of development and is rapidly moving as it is applied across a variety of user interfaces and approaches to API operations and governance. If you would like to contribute, have any questions, or would like to inform the work happening, please submit a GitHub issue on this repository or email kin@apievangelist.com.

## Part of API Commons

A machine-readable building block from **[API Commons](https://apicommons.org)** — open specifications and schemas for the APIs you produce and consume. See all building blocks and tools at **[apicommons.org](https://apicommons.org)** and the tools at **[apicommons.org/tools](https://apicommons.org/tools/)**.

**Related building blocks**
- [teams](https://github.com/api-commons/teams) — the people layer of API operations
- [policies](https://github.com/api-commons/policies) — the business rules behind API governance
- [guidance](https://github.com/api-commons/guidance) — the how-to layer that turns governance rules into help
- [plans](https://github.com/api-commons/plans) — machine-readable access plans, tiers, and pricing
- [road-map](https://github.com/api-commons/road-map) — publish an API's roadmap in a machine-readable way

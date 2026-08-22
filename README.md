# Direct Line Group (direct-line-group)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Direct Line Group is a United Kingdom personal-lines and small-commercial general insurance carrier, founded in 1985 as the UK's first telephone-only motor insurer and listed on the London Stock Exchange from its 2012 IPO until Aviva plc completed its GBP 3.7 billion acquisition of the group on 1 July 2025. The group underwrites motor, home, pet, travel, landlord, breakdown and small-business insurance through the Direct Line, Churchill, Privilege, Darwin, By Miles, Direct Line for Business and Green Flag brands, and is regulated in its home market by the Financial Conduct Authority and the Prudential Regulation Authority.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/direct-line-group/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/direct-line-group/refs/heads/main/apis.yml)

## Tags

- Insurance
- United Kingdom
- Property and Casualty
- Personal Lines
- Motor Insurance
- Home Insurance
- Carrier
- Roadside Assistance
- Partner Gated

## Timestamps

- **Created:** 2026-07-25
- **Modified:** 2026-07-25

## APIs

**None.** Direct Line Group publishes no public, self-serve API and no developer portal. This is not an omission in the record — it is the finding.

What was probed on 2026-07-25:

- `directlinegroup.co.uk` and `www.directlinegroup.co.uk` return **HTTP 301 to https://www.aviva.com/**. The corporate site was retired into Aviva after the acquisition completed on 1 July 2025, so every historical `/developers`, `/api`, `/developer`, `/partners` and `/integrations` path now lands on the Aviva homepage.
- `developer.`, `developers.` and `docs.directlinegroup.co.uk` do not exist in DNS (NXDOMAIN).
- `api.directlinegroup.co.uk` **does** exist and resolves to `dlg-production-load-balancer.lb.anypointdns.net` — a **MuleSoft Anypoint Platform** production load balancer. It serves **HTTP 403 Forbidden** at the root, behind an **expired TLS certificate**, and **requests a client certificate during the TLS handshake (mutual TLS)**. `/openapi.json`, `/swagger.json`, `/api-docs`, `/console`, `/health` and `/status` are all 404. This is an internal and partner integration gateway, not a developer surface.
- Every live consumer brand site — [directline.com](https://www.directline.com/), [churchill.com](https://www.churchill.com/), [greenflag.com](https://www.greenflag.com/), [privilege.com](https://www.privilege.com/), [darwin-insurance.com](https://www.darwin-insurance.com/), [bymiles.co.uk](https://www.bymiles.co.uk/), [directlineforbusiness.co.uk](https://www.directlineforbusiness.co.uk/) — returns 404 on `/developers`, `/api` and `/partners`.
- `docs.directline.com` returns HTTP 200 but is a **login wall** titled "DirectLine - Login", with no reference documentation. It is not a developer portal.
- No OpenAPI or Swagger document, no GraphQL endpoint, no gRPC or `.proto`, no AsyncAPI, no webhook or event catalog, no public Postman workspace. No `/.well-known/openid-configuration` or `/.well-known/oauth-authorization-server` on any brand host.
- [github.com/Direct-Line-Group](https://github.com/Direct-Line-Group) exists (created 2019-07-03, "Direct Line org for all new code Projects") with **zero public repositories**.

### Enrichment round, 2026-07-25

A second, wider pass re-confirmed the "no public API" finding and changed three things.

- **A second gated API host exists.** `api.bymiles.co.uk` resolves and is an **Amazon API Gateway** deployment — the root returns HTTP 403 `{"message":"Forbidden"}` with `x-amzn-errortype: ForbiddenException` and an `x-amz-apigw-id` header, and `/v1/*` returns `{"message":"Missing Authentication Token"}`. Its certificate is valid. It is gated and undocumented, but it establishes a second, AWS-based integration estate alongside the group's MuleSoft gateway. `api.darwin.co.uk` also resolves to AWS anycast addresses but presents no certificate for that SNI name.
- **`www.darwin.co.uk` is not a group property**, and was recorded in error in the first pass. It redirects to `forsale.godaddy.com` and its `/llms.txt` is a GoDaddy aftermarket for-sale notice. The real Darwin brand site is **[www.darwin-insurance.com](https://www.darwin-insurance.com/)**, whose footer states policies are underwritten by U K Insurance Limited (FCA No. 536726) and arranged and administered by iGO4 Limited.
- **The group privacy notice was located** at [brandsprivacypolicy.co.uk/policy](https://www.brandsprivacypolicy.co.uk/policy) — published by U K Insurance Limited and covering Direct Line, Churchill, Privilege, Darwin and Green Flag.

Everything else re-confirmed negative: 49 `/.well-known/` probes across 11 hosts returned **zero** discovery documents (the HTTP 200s on `www.privilege.com` and `docs.directline.com` are soft 404s serving HTML templates, verified by body inspection); no `security.txt`; no first-party package on npm, PyPI, Maven Central, NuGet, pkg.go.dev, RubyGems, Packagist or crates.io — note that npm hits for "direct-line" are all Microsoft Bot Framework **Direct Line** chat-protocol clients, an unrelated namespace collision; no vulnerability-disclosure programme and no trust center.

## Artifacts

| Artifact | File | Method |
|---|---|---|
| Domain security | [`security/direct-line-group-domain-security.yml`](security/direct-line-group-domain-security.yml) | probed |
| Well-known probe matrix | [`well-known/direct-line-group-well-known.yml`](well-known/direct-line-group-well-known.yml) | probed (zero documents) |
| Conformance | [`conformance/direct-line-group-conformance.yml`](conformance/direct-line-group-conformance.yml) | derived |
| Packages | [`packages/direct-line-group-packages.yml`](packages/direct-line-group-packages.yml) | searched (none exist) |
| llms.txt | [`llms/direct-line-group-llms.txt`](llms/direct-line-group-llms.txt) | generated |

No `openapi/`, `asyncapi/`, `graphql/`, `mcp/`, `skills/`, `scopes/`, `authentication/`, `sandbox/`, `changelog/`, `cli/`, `errors/` or `lifecycle/` artifact exists, because there is no machine-readable contract and no published developer documentation to ground one in. Fabricating any of them would be the wrong outcome for this record.

## ACORD Posture

**No ACORD reference found.** Nothing referencing ACORD, AL3, ACORD XML, ACORD certification or NGDS appears on any Direct Line Group or brand property. That is consistent with the UK personal-lines market, where broker/insurer data exchange runs on **Polaris Standards** and the **imarket** platform rather than on ACORD — and Direct Line Group is a direct writer that exited the brokered commercial channel entirely when it sold NIG and FarmWeb to RSA in September 2023.

## Quote / Bind / Issue / FNOL

None of the four insurance verbs is exposed through a public API. Quote and bind are consumer web and telephone journeys plus price-comparison-website placement (notably via the Darwin brand); issue and FNOL happen in logged-in customer self-service and by phone.

## Market Context

The UK has the FCA and PRA but **no open-insurance obligation** — the FCA's Open Finance work is still consultation, not rule. The country's only market-wide data and API infrastructure effort is the **London Market** modernization programme (Blueprint Two, PPL, Whitespace, Ki), and it is aimed at brokers and syndicates in the subscription market, not at developers. Direct Line Group does not participate in that market. As a direct-to-consumer carrier with no broker channel, it sits outside every seam that would otherwise produce a public API.

## Links

- [Direct Line](https://www.directline.com/)
- [Churchill](https://www.churchill.com/)
- [Green Flag](https://www.greenflag.com/)
- [Privilege](https://www.privilege.com/)
- [Darwin](https://www.darwin-insurance.com/)
- [By Miles](https://www.bymiles.co.uk/)
- [Direct Line for Business](https://www.directlineforbusiness.co.uk/)
- [Aviva plc (parent)](https://www.aviva.com/)
- [GitHub organization](https://github.com/Direct-Line-Group)
- [Help and support](https://www.directline.com/help)
- [Website terms of use](https://www.directline.com/legal/terms)
- [Privacy notice (U K Insurance Limited)](https://www.brandsprivacypolicy.co.uk/policy)
- [Direct Line Magazine](https://www.directline.com/magazine)
- [By Miles partnerships](https://www.bymiles.co.uk/partners)

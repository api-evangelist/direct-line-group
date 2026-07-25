# Direct Line Group (direct-line-group)

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
- Every live consumer brand site — [directline.com](https://www.directline.com/), [churchill.com](https://www.churchill.com/), [greenflag.com](https://www.greenflag.com/), [privilege.com](https://www.privilege.com/), [darwin.co.uk](https://www.darwin.co.uk/), [bymiles.co.uk](https://www.bymiles.co.uk/), [directlineforbusiness.co.uk](https://www.directlineforbusiness.co.uk/) — returns 404 on `/developers`, `/api` and `/partners`.
- `docs.directline.com` returns HTTP 200 but is a **login wall** titled "DirectLine - Login", with no reference documentation. It is not a developer portal.
- No OpenAPI or Swagger document, no GraphQL endpoint, no gRPC or `.proto`, no AsyncAPI, no webhook or event catalog, no public Postman workspace. No `/.well-known/openid-configuration` or `/.well-known/oauth-authorization-server` on any brand host.
- [github.com/Direct-Line-Group](https://github.com/Direct-Line-Group) exists (created 2019-07-03, "Direct Line org for all new code Projects") with **zero public repositories**.

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
- [Darwin](https://www.darwin.co.uk/)
- [By Miles](https://www.bymiles.co.uk/)
- [Direct Line for Business](https://www.directlineforbusiness.co.uk/)
- [Aviva plc (parent)](https://www.aviva.com/)
- [GitHub organization](https://github.com/Direct-Line-Group)

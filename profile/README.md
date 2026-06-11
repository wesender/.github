# WeSender

**Transactionele e-mail API voor Nederland en Europa.**  
Verstuur welkomstmails, facturen, wachtwoordresets en meer — via één REST API, SMTP of SDK.

---

## SDK's

| Taal | Repo | Installatie |
|------|------|-------------|
| **Node.js / TypeScript** | [wesender-node](https://github.com/wesender/wesender-node) | `npm install @wesender/wesender-node` |
| **Python** | [wesender-python](https://github.com/wesender/wesender-python) | `pip install wesender` |
| **PHP** | [wesender-php](https://github.com/wesender/wesender-php) | `composer require wesender/wesender` |
| **Go** | [wesender-go](https://github.com/wesender/wesender-go) | `go get github.com/wesender/wesender-go` |
| **Ruby** | [wesender-ruby](https://github.com/wesender/wesender-ruby) | `gem install wesender` |
| **Rust** | [wesender-rust](https://github.com/wesender/wesender-rust) | `cargo add wesender` |
| **Java** | [wesender-java](https://github.com/wesender/wesender-java) | `nl.wesender:wesender-java:1.0.0` |
| **.NET / C#** | [wesender-dotnet](https://github.com/wesender/wesender-dotnet) | `dotnet add package Wesender` |
| **Elixir** | [wesender-elixir](https://github.com/wesender/wesender-elixir) | `{:wesender, "~> 1.0"}` |
| **CLI** | [wesender-cli](https://github.com/wesender/wesender-cli) | `npm install -g @wesender/wesender-cli` |

## Snel aan de slag

```typescript
import { Wesender } from "@wesender/wesender-node"

const ws = new Wesender(process.env.WS_API_KEY!)

await ws.emails.send({
  from:    "noreply@joudomein.nl",
  to:      "klant@voorbeeld.nl",
  subject: "Welkom!",
  html:    "<p>Bedankt voor je registratie.</p>",
})
```

## CLI

```bash
# Installeren
npm install -g @wesender/wesender-cli

# Configureren
wesender config set-key ws_live_...

# Testmail versturen
wesender send --to jij@voorbeeld.nl --subject "Test" --html "<p>Hallo!</p>"

# Domeinen bekijken
wesender domains list

# Verbinding controleren
wesender doctor
```

## Functies

- **Hoge deliverability** — DKIM, SPF en DMARC automatisch geconfigureerd
- **Domeinbeheer** — voeg domeinen toe en verifieer DNS via de API
- **Webhooks** — realtime events bij bezorging, opening, bounces en klikken
- **SMTP-relay** — werkt plug & play met elke bestaande mail-library
- **Batches** — stuur tot 100 e-mails in één aanroep
- **AVG-compliant** — infrastructuur volledig gehost in Nederland

## Links

- [Documentatie](https://docs.wesender.nl)
- [API-referentie](https://docs.wesender.nl/api-reference/emails)
- [Statuspage](https://status.wesender.nl)
- [Support](https://support.wesender.nl)
- [Dashboard](https://app.wesender.nl)

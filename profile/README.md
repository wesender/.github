# WeSender

**Transactionele e-mail API voor Nederland en Europa.**  
Verstuur welkomstmails, facturen, wachtwoordresets en meer — via één API of SMTP.

---

## SDK's

| Taal | Repo | Installatie |
|------|------|-------------|
| **Node.js / TypeScript** | [wesender-node](https://github.com/nljerry/wesender-node) | `npm install @nljerry/wesender-node` |
| **Python** | [wesender-python](https://github.com/nljerry/wesender-python) | `pip install wesender` |
| **PHP** | [wesender-php](https://github.com/nljerry/wesender-php) | `composer require wesender/wesender` |
| **Go** | [wesender-go](https://github.com/nljerry/wesender-go) | `go get github.com/nljerry/wesender-go` |
| **Ruby** | [wesender-ruby](https://github.com/nljerry/wesender-ruby) | `gem install wesender` |
| **CLI** | [wesender-cli](https://github.com/nljerry/wesender-cli) | `npm install -g @nljerry/wesender-cli` |

## Snel aan de slag

```typescript
import { Wesender } from "@nljerry/wesender-node"

const ws = new Wesender(process.env.WS_API_KEY!)

await ws.emails.send({
  from:    "noreply@joudomein.nl",
  to:      "klant@voorbeeld.nl",
  subject: "Welkom!",
  html:    "<p>Bedankt voor je registratie.</p>",
})
```

## Functies

- **Hoge deliverability** — DKIM, SPF en DMARC geconfigureerd
- **Domeinbeheer** — voeg domeinen toe en verifieer ze via de API
- **Webhooks** — ontvang events bij levering, opening en bounces
- **SMTP-ondersteuning** — werkt met elke bestaande mail-library
- **Batches** — stuur duizenden e-mails in één aanroep
- **AVG-compliant** — data opgeslagen in Nederland

## Links

- [Documentatie](https://wesender.nl/docs)
- [API-referentie](https://wesender.nl/docs/api-reference/emails)
- [Statuspage](https://wesender.nl/status)
- [Dashboard](https://app.wesender.nl)

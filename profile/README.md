<p align="center">
  <a href="https://loglayer.dev"><img src="https://loglayer.dev/images/loglayer.png" alt="LogLayer" width="150" /></a>
</p>

<h3 align="center">A unified logging layer for TypeScript / JavaScript</h3>

<p align="center">
  <a href="https://www.npmjs.com/package/loglayer"><img src="https://img.shields.io/npm/v/loglayer.svg?style=flat-square" alt="NPM version" /></a>
  <a href="https://www.npmjs.com/package/loglayer"><img src="https://img.shields.io/npm/dm/loglayer" alt="NPM Downloads" /></a>
  <a href="http://www.typescriptlang.org/"><img src="https://img.shields.io/badge/%3C%2F%3E-TypeScript-%230074c1.svg" alt="TypeScript" /></a>
  <img src="https://img.shields.io/bundlejs/size/loglayer" alt="Bundle size" />
  <a href="https://github.com/loglayer/loglayer/blob/master/LICENSE"><img src="https://img.shields.io/github/license/loglayer/loglayer" alt="MIT License" /></a>
</p>

<p align="center">
  <a href="https://loglayer.dev">Documentation</a> &bull;
  <a href="https://loglayer.dev/getting-started">Getting Started</a> &bull;
  <a href="https://github.com/loglayer/loglayer">GitHub</a>
</p>

---

**LogLayer** provides a fluent, structured logging API that sits on top of your logging library of choice. Fan out logs to multiple destinations at the same time — start with `console`, then add Pino, Datadog, or any combination of transports without changing your application code.

```typescript
import { LogLayer } from 'loglayer';
import { PinoTransport } from '@loglayer/transport-pino';
import { DatadogTransport } from '@loglayer/transport-datadog';
import pino from 'pino';

const log = new LogLayer({
  // Send logs to multiple destinations at the same time
  transport: [
    new PinoTransport({ logger: pino() }),
    new DatadogTransport({
      apiKey: process.env.DD_API_KEY,
      service: 'my-app',
    }),
  ],
});

log.withContext({ requestId: 'abc-123' })
   .withMetadata({ duration: 150 })
   .withError(new Error('Timeout'))
   .error('Request failed');
```

### Highlights

- **Bring your own logger** — works with Pino, Winston, Bunyan, tslog, Consola, and more
- **Multi-transport** — send logs to multiple destinations simultaneously (e.g. Pino + Datadog)
- **Cloud-native** — transports for Datadog, AWS CloudWatch, Google Cloud, New Relic, Sentry, Axiom, Better Stack, and others
- **Extensible** — plugins for redaction, filtering, OpenTelemetry trace injection, and sprintf formatting
- **Framework integrations** — first-class support for Hono, Fastify, and ElysiaJS
- **Multi-platform** — runs on Node.js, Deno, Bun, and browsers
- **Tiny footprint** — 8kB gzipped core, most transports under 1kB
- **Battle tested** — in production for 4+ years at [Airtop.ai](https://airtop.ai)

### Ecosystem

| | Packages |
|---|---|
| **Logging Libraries** | Pino, Winston, Bunyan, Consola, tslog, Log4js, Roarr, Signale, loglevel, LogTape, Tracer, Electron-log |
| **Cloud Providers** | Datadog, AWS CloudWatch, AWS Lambda Powertools, Google Cloud, New Relic, Sentry, Axiom, Better Stack, Dynatrace, Sumo Logic, Logflare, VictoriaLogs |
| **Other Transports** | HTTP, Log File Rotation, OpenTelemetry, Pretty Terminal, Simple Pretty Terminal |
| **Plugins** | Redaction, Filter, OpenTelemetry, Datadog APM Trace Injector, Sprintf |
| **Integrations** | Hono, Fastify, ElysiaJS |
| **Mixins** | Hot-Shots (StatsD), Datadog Metrics (HTTP) |

### Get Started

```bash
npm install loglayer
```

Read the [documentation](https://loglayer.dev) or jump straight to the [getting started guide](https://loglayer.dev/getting-started).

---

<sub>Made with care by <a href="https://suteki.nu">Theo Gravity</a>. Logo by <a href="https://www.linkedin.com/in/akshaya-madhavan">Akshaya Madhavan</a>.</sub>

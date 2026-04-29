<p align="center">
  <a href="https://loglayer.dev"><img src="https://loglayer.dev/images/loglayer.png" alt="LogLayer" width="150" /></a>
</p>

<h1 align="center">LogLayer</h1>

<h3 align="center">A unified, transport-agnostic structured logging API</h3>

<p align="center">
  Fluent calls for messages, metadata, and errors.<br>
  Bring your own underlying logger. Send to multiple destinations at once.
</p>

<p align="center">
  Available for <strong>TypeScript / JavaScript</strong> and <strong>Go</strong>.
</p>

---

### TypeScript / JavaScript

<p>
  <a href="https://www.npmjs.com/package/loglayer"><img src="https://img.shields.io/npm/v/loglayer.svg?style=flat-square" alt="NPM version" /></a>
  <a href="https://www.npmjs.com/package/loglayer"><img src="https://img.shields.io/npm/dm/loglayer" alt="NPM Downloads" /></a>
  <a href="http://www.typescriptlang.org/"><img src="https://img.shields.io/badge/%3C%2F%3E-TypeScript-%230074c1.svg" alt="TypeScript" /></a>
  <img src="https://img.shields.io/bundlejs/size/loglayer" alt="Bundle size" />
  <a href="https://github.com/loglayer/loglayer/blob/master/LICENSE"><img src="https://img.shields.io/github/license/loglayer/loglayer" alt="MIT License" /></a>
</p>

<p>
  <a href="https://loglayer.dev"><strong>Documentation</strong></a> &bull;
  <a href="https://loglayer.dev/getting-started">Getting Started</a> &bull;
  <a href="https://github.com/loglayer/loglayer">GitHub</a>
</p>

### Go

<p>
  <a href="https://github.com/loglayer/loglayer-go/releases"><img src="https://img.shields.io/github/v/tag/loglayer/loglayer-go?filter=v*&amp;sort=semver&amp;label=version&amp;style=flat-square" alt="Latest version" /></a>
  <a href="https://pkg.go.dev/go.loglayer.dev"><img src="https://pkg.go.dev/badge/go.loglayer.dev.svg" alt="Go Reference" /></a>
  <a href="https://github.com/loglayer/loglayer-go"><img src="https://img.shields.io/github/go-mod/go-version/loglayer/loglayer-go" alt="Go version" /></a>
  <a href="https://github.com/loglayer/loglayer-go/blob/main/LICENSE"><img src="https://img.shields.io/github/license/loglayer/loglayer-go" alt="MIT License" /></a>
</p>

<p>
  <a href="https://go.loglayer.dev"><strong>Documentation</strong></a> &bull;
  <a href="https://go.loglayer.dev/getting-started">Getting Started</a> &bull;
  <a href="https://github.com/loglayer/loglayer-go">GitHub</a>
</p>

---

### Highlights

Both implementations share the same design ideas:

- **Bring your own logger** — wraps Pino / Winston / Bunyan / Consola / tslog / ... (TS) and Zerolog / Zap / log/slog / phuslu / logrus / charmlog (Go)
- **Multi-transport** — fan out the same log to several destinations at once
- **Cloud-native** — first-class transports for Datadog, OpenTelemetry, and others
- **Extensible** — plugins for redaction, sampling, trace injection, and more

---

<sub>Made with care by <a href="https://suteki.nu">Theo Gravity</a>. Logo by <a href="https://www.linkedin.com/in/akshaya-madhavan">Akshaya Madhavan</a>.</sub>

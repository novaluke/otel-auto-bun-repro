# OpenTelemetry issues in Bun

To test OpenTelemetry auto-instrumentation in Bun:

```bash
bun install
bun run start
curl localhost:8080/rolldice
```

Compare the output with auto-instrumentation in NodeJS:

```bash
bun run start:cjs # OR start:mjs
curl localhost:8080/rolldice
```

Running via Bun produces a single span for `GET`, whereas running via NodeJS
produces sub-spans for the express functions and middleware.

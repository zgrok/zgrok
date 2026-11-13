# zgrok

**Expose localhost to the internet with one command.** zgrok gives a server running on your machine a public HTTPS URL, with live request inspection and replay built in.

Website: **[zgrok.io](https://www.zgrok.io)** · Docs: **[zgrok.io/docs](https://www.zgrok.io/docs)** · Pricing: **[zgrok.io/pricing](https://www.zgrok.io/pricing)**

```bash
zgrok http 3000
# https://api--acme-shop.zgrok.io -> http://localhost:3000
```

## Install

macOS (Apple Silicon) and Linux (x64):

```bash
curl -fsSL https://zgrok.io/install.sh | sh
```

Windows (PowerShell):

```powershell
irm https://zgrok.io/install.ps1 | iex
```

Then sign in and start a tunnel:

```bash
zgrok login
zgrok http 3000
```

Every release is signed, and the CLI and both installers verify the signature before installing anything. Manual downloads: [downloads.zgrok.io](https://downloads.zgrok.io).

## What it does

- **Public HTTPS URL for any local port.** Webhooks, mobile testing on a real phone, sharing a work-in-progress app.
- **Request inspector.** Every request through the tunnel, with headers and bodies, in a local web UI at `127.0.0.1:4040`. Replay any of them with one click.
- **Built on QUIC.** The CLI talks to the relay over QUIC, so connection setup and TLS 1.3 happen in a single round trip and one slow request never blocks the others.
- **WebSockets and streaming responses** pass through unchanged.
- **Expose a local AI model** (`zgrok ai`): put Ollama, LM Studio, vLLM or llama.cpp behind a public URL with token authentication on by default.
- **Access control:** Basic Auth and IP allowlists in front of a tunnel, plus custom response headers.
- **Projects and teams:** every tunnel lives in a project, shared with your organization.

## Plans

**Free** needs no card and runs more than one tunnel at a time, with unlimited data and requests
and a window of request history. **Pro** raises the tunnel count, keeps a custom tunnel name
across sessions, and adds password protection, IP allowlists and a longer history window.

Every limit and the current price: [zgrok.io/pricing](https://www.zgrok.io/pricing)

## Help

- Documentation: [zgrok.io/docs](https://www.zgrok.io/docs)
- Support: support@zgrok.io
- Security reports: security@zgrok.io
- Updates: [@zgrokio on X](https://x.com/zgrokio)

---

zgrok is built and run by [zgrok.io](https://www.zgrok.io). It is not affiliated with other projects that use a similar name.

# adacode

> **adaCODE CLI** — All-in-one AI coding platform.  
> Login, setup, manage dashboard & API keys dari satu command.

[![npm](https://img.shields.io/npm/v/adacode)](https://www.npmjs.com/package/adacode)
[![npm downloads](https://img.shields.io/npm/dm/adacode)](https://www.npmjs.com/package/adacode)

## Install

```bash
npm install -g adacode
```

Atau gunakan langsung tanpa install:
```bash
npx adacode
```

## Quick Start

```bash
# 1. Login via browser (auto API key)
adacode login

# 2. Setup CLI tool favorit Anda
adacode setup claude     # Claude Code
adacode setup codex      # CodeX
adacode setup opencode   # OpenCode
adacode setup openclaw   # OpenClaw

# 3. Mulai coding!
claude    # atau: codex, opencode
```

## Semua Commands

| Command | Fungsi |
|---------|--------|
| `adacode login` | Login via browser → otomatis simpan API key |
| `adacode setup` | Interactive wizard — pilih CLI & konfigurasi |
| `adacode setup claude` | Setup Claude Code saja |
| `adacode setup codex` | Setup CodeX saja |
| `adacode setup opencode` | Setup OpenCode saja |
| `adacode setup openclaw` | Setup OpenClaw saja |
| `adacode start` | Start dashboard service (auto-download) |
| `adacode stop` | Stop dashboard service |
| `adacode status` | Status: login, plan, quota, service |
| `adacode models` | List model AI tersedia |
| `adacode apikey` | Tampilkan API key Anda |
| `adacode autostart on\|off` | Auto-start dashboard saat boot |
| `adacode update` | Update CLI ke versi terbaru |

## Persyaratan

- **Node.js** v18+
- **Akun adaCODE** — daftar gratis di [adacode.ai](https://adacode.ai)

## CLI Tools yang Didukung

| CLI | Kegunaan | Setelah Setup |
|-----|----------|---------------|
| **Claude Code** | Coding assistant Anthropic | `claude` |
| **CodeX** | Coding assistant OpenAI | `codex` |
| **OpenCode** | Terminal IDE berbasis AI | `opencode` |
| **OpenClaw** | AI Gateway (WhatsApp, Telegram, dll.) | `npx openclaw gateway --bind lan` |

## Model yang Tersedia

| Model | Provider |
|-------|----------|
| Qwen3 Coder Plus | Alibaba |
| Qwen3.5 Plus | Alibaba |
| Claude Sonnet 4.6 | Anthropic |
| Claude Opus 4.6 | Anthropic |
| GPT-5.3 | OpenAI |
| GLM-4.7 | Zhipu AI |
| MiniMax M2.5 | MiniMax |

> Lihat daftar terbaru: `adacode models`

## Setup Detail

### Claude Code

```bash
adacode setup claude
```

File yang ditulis:
- `~/.claude/settings.json` — API key + base URL
- Environment variables — `ANTHROPIC_AUTH_TOKEN`, `ANTHROPIC_BASE_URL`
- `~/.claude/CLAUDE.md` — Auto-memory system

### CodeX

```bash
adacode setup codex
```

File yang ditulis:
- `~/.codex/config.toml` — model provider
- `~/.codex/auth.json` — API key

### OpenCode

```bash
adacode setup opencode
```

File yang ditulis:
- `~/.config/opencode/opencode.json` — provider config + models

### OpenClaw

```bash
adacode setup openclaw
```

File yang ditulis:
- `~/.openclaw/openclaw.json` — provider, models, gateway token

---

## Fitur

- **One-line login** — `adacode login` buka browser, auto-save API key
- **Free plan** — Login → otomatis dapat Free plan + API key
- **Bilingual** — English & Bahasa Indonesia (auto-detect)
- **Safe backup** — File `.bak` otomatis sebelum overwrite
- **Cross-platform** — Windows, macOS, Linux
- **Dashboard** — `adacode start` untuk monitoring usage & model

## Troubleshooting

### "Not logged in" setelah setup
- **Windows:** Tutup dan buka ulang terminal
- **macOS/Linux:** `source ~/.bashrc` atau buka terminal baru

### Claude Code: Auth conflict
```bash
claude /logout   # Hapus session lama
adacode setup claude   # Setup ulang
```

### Model tidak muncul
```bash
adacode models   # Cek model tersedia
adacode status   # Cek status login & quota
```

## Links

- **Website:** [adacode.ai](https://adacode.ai)
- **Docs:** [adacode.ai/vibe-coding](https://adacode.ai/vibe-coding)
- **NPM:** [npmjs.com/package/adacode](https://www.npmjs.com/package/adacode)

## License

MIT

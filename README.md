# rig

Keeps a lane's lights on while nobody is in it: a heartbeat every minute, a status board, and
(next) a morning digest of what ran overnight.

```sh
cp .env.example .env   # set LANE_MARKER
pnpm install
pnpm dev               # http://localhost:8787
```

Working on it with an agent: start at [AGENTS.md](AGENTS.md).

## Model credential

Agents that run in CI need a model key in the repo's secrets. Any vendor works.

No paid plan? A free Google AI Studio key works through its OpenAI-compatible endpoint
(`https://generativelanguage.googleapis.com/v1beta/openai`). Use `gemini-flash-lite-latest`:
`gemini-flash-latest` runs dry at about 20 calls a day, and every agent in this repo shares the one key.
The live quota is on the key's page in AI Studio.

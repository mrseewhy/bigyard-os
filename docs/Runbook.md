# Local Runbook

**These are setup steps, not proof tools are installed.** Target Apple Silicon 16 GB Mac.

```bash
git clone https://github.com/mrseewhy/bigyard-os.git
cd bigyard-os
git --version
docker --version
docker compose version
node --version
npm --version
ffmpeg -version
ollama --version
```

Install missing prerequisites from official sources, confirm version compatibility for n8n and Remotion, and keep local Ollama models small. Use local loopback bindings for n8n/Postgres. After Docker Compose is implemented in T005, run `docker compose up -d`, then `docker compose ps` and check logs. Do not claim the compose file already exists.

When .env.example has been copied to .env, add credentials **only locally** and never commit the real file. Turn off external publishing and paid API calls until permissions and explicit approval are established. Version workflow JSON without credentials.

Test: local job lifecycle, restart persistence, simulated timeout and duplicate prevention, actual media inspect, rejected approval blocks publishing, account eligibility and API scope. When laptop sleeps, schedules cannot run; provide missed-job alerts upon resumption. Back up and test restoring volumes before relying on operations.

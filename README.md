# FB-TRACER-OSINT-TOOLS-
Disclamer: this is a vibe coded program python program FB-TRACER(OSINT TOOLS) . it may not give you a 100% accuracy. 
# fbtracer

Public-data Facebook profile resolver. Walang login, walang API key na kailangan.

**Developed by Joshua D. Gordon**

## Install — Parrot OS

chmod +x run.sh
python3 -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
cp .env.example .env

## Run

./run.sh about
./run.sh demo
./run.sh juan.dela.cruz
./run.sh "Juan Dela Cruz"
./run.sh https://facebook.com/juan.dela.cruz
./run.sh 100000000000001


## Web dashboard

./run.sh web


Buksan ang http://127.0.0.1:5000

## Flags

| Flag | Gamit |
|---|---|
| `--save` | i-save ang HTML + JSON report sa `reports/` |
| `--json` | JSON output lang |
| `--token <t>` | Graph API token |

## Ano ang kaya

| Data | Status |
|---|---|
| Profile URL mula sa pangalan | ✅ |
| Username ↔ numeric ID | ✅ |
| Pangalan, bio, trabaho, eskwelahan | ✅ kung public |
| Profile picture (720px) | ✅ kahit private |
| Email / phone | ⚠️ kung nasa public About |

Hindi kaya: email/phone ng fully-locked profile. Kailangan niyan ng Graph token.

## Troubleshooting

| Problema | Solusyon |
|---|---|
| LookupError | Buksan ang FB, hanapin manually, i-paste ang exact URL |
| 429 / blangko | Taasan ang `REQUEST_DELAY` sa `.env` |
| Mababang confidence | Mag-paste ng direct link |

---

fbtracer 1.0.0 — developed by Joshua D. Gordon. Hindi affiliated sa Meta.


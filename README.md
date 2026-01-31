# Institutional Perps Arbitrage Bot


Institutional Perps Arbitrage Bot - Production Entry Point
Dynamic event discovery + Morpho vaults + 24/7 human oversight


[![CI](https://github.com/workflows/CI/badge.svg)](https://github.com/actions)

**$100K → 20% annual returns** | Dynamic events | Morpho vaults | Telegram control

## Quick Start
```bash
cp config/production.yaml.example config/production.yaml
# Edit API keys
docker-compose up

## GitHub Repository Structure (Production-Ready)

institutional-perps-arb-bot/
├── 📁 src/                          # Source code
│   ├── __init__.py
│   ├── main.py                      # Entry point (complete_arb_bot.py)
│   ├── core/
│   │   ├── __init__.py
│   │   ├── arbitrage_engine.py      # Core arb detection + execution
│   │   ├── event_classifier.py      # Dynamic event discovery AI
│   │   └── risk_manager.py          # Circuit breakers + position sizing
│   ├── exchanges/
│   │   ├── __init__.py
│   │   ├── binance_client.py        # CCXT Binance wrapper
│   │   ├── bitmex_client.py         # CCXT BitMEX wrapper
│   │   └── kalshi_client.py         # Kalshi prediction markets
│   ├── defi/
│   │   ├── __init__.py
│   │   └── morpho_vaults.py         # Morpho vault infrastructure
│   └── oversight/
│       ├── __init__.py
│       └── telegram_controller.py   # Human oversight interface
├── 📁 config/                       # Configuration
│   ├── production.env.example       # Env vars template
│   ├── development.env.example      # Dev template
│   └── config.yaml                  # YAML config override
├── 📁 docker/                       # Containerization
│   ├── Dockerfile.prod              # Production Docker
│   ├── Dockerfile.dev               # Development Docker
│   └── docker-compose.prod.yml      # Production stack (bot + Redis)
├── 📁 scripts/                      # Automation
│   ├── deploy.sh                    # One-click production deploy
│   ├── backtest.py                  # Historical backtesting
│   └── health_check.py              # Monitoring script
├── 📁 tests/                        # Unit/integration tests
│   ├── test_arbitrage_engine.py
│   ├── test_event_classifier.py
│   └── test_risk_manager.py
├── 📁 docs/                         # Documentation
│   ├── DEPLOYMENT.md                # Production guide
│   ├── TRADING.md                   # Strategy explanation
│   └── API.md                       # Internal API docs
├── 📁 monitoring/                   # Observability
│   ├── prometheus.yml               # Metrics export
│   └── grafana-dashboard.json       # Pre-built dashboard
├── 🗄️ requirements.txt              # Python dependencies
├── 🗄️ requirements-dev.txt          # Dev dependencies
├── 🗄️ .gitignore                    # Git exclusions
├── 🗄️ README.md                     # Main repo documentation
├── 🗄️ LICENSE                       # MIT/Apache 2.0
├── 🗄️ .github/
│   └── workflows/
│       ├── ci.yml                   # CI/CD pipeline
│       └── deploy-staging.yml       # Auto-deploy to staging
└── 🗄️ docker-compose.yml           # Local development

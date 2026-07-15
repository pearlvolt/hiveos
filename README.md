# PearlVolt for HiveOS

🌐 https://pearlvolt.run
💬 Discord: https://discord.gg/ZRSBaSMtg

Install PearlVolt miner on HiveOS.

## Installation

### Custom Miner

1. HiveOS web → Worker → Miner → Custom
2. Set:
   - **Miner name**: `pearlvolt`
   - **Install URL**: `https://github.com/pearlvolt/hiveos/releases/download/v1.0.0/pearlvolt-1.0.0.tar.gz`
   - **Wallet**: `WALLET:prl1YOURWALLETADDRESS`
   - **Pool**: `stratum+tcp://pool.pearlvolt.run:4141`

### Manual

```bash
wget https://github.com/pearlvolt/hiveos/releases/latest/download/pearlvolt
chmod +x pearlvolt
./pearlvolt --pool stratum+tcp://pool.pearlvolt.run:4141 --wallet prl1YOURWALLETADDRESS
```

## Telemetry

```bash
curl http://localhost:4141
```

## Supported GPUs

| GPU | Hashrate | Power |
|-----|----------|-------|
| RTX 5090 | 390 TH/s | 600 W |
| RTX 4090 | 255 TH/s | 450 W |
| RTX 3090 | 120 TH/s | 350 W |

## Requirements

- HiveOS (recent version)
- NVIDIA driver 535+ (595+ for RTX 5090)
- No CUDA toolkit needed

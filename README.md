# PearlVolt HiveOS

PearlVolt miner packaged for HiveOS. Install via custom miner or download the binary directly.

## Installation

### Option 1: Custom Miner (recommended)

1. Go to HiveOS web → Workers → your worker → Miner
2. Select "Custom"
3. Set:
   - **Miner name**: `pearlvolt`
   - **Install URL**: `https://github.com/pearlvolt/hiveos/releases/latest/download/pearlvolt-hiveos.tar.gz`
   - **Hash algorithm**: `pearlvolt`
   - **Wallet configuration**: `WALLET:prl1YOURWALLETADDRESS`
   - **Pool configuration**: `stratum+tcp://pool.pearlvolt.run:4141`

### Option 2: Manual download

```bash
# SSH into your HiveOS rig
wget https://github.com/pearlvolt/hiveos/releases/latest/download/pearlvolt
chmod +x pearlvolt
./pearlvolt --pool stratum+tcp://pool.pearlvolt.run:4141 --wallet prl1YOURWALLETADDRESS --gpus 0,1,2
```

## Telemetry

The miner serves live stats on `http://localhost:4141`:

```bash
curl http://localhost:4141
```

## Supported GPUs

| GPU | Hashrate | Power |
|-----|----------|-------|
| RTX 5090 | 390 TH/s | 600 W |
| RTX 4090 | 255 TH/s | 450 W |
| RTX 3090 | 120 TH/s | 350 W |
| H100 | 736 TH/s | 700 W |
| H200 | 762 TH/s | 700 W |

## Requirements

- HiveOS (any recent version)
- NVIDIA driver 535+ (driver 595+ for RTX 5090)
- No CUDA toolkit needed — static runtime built-in

## Configuration

| Parameter | Default | Description |
|-----------|---------|-------------|
| `--pool` | herominers | Pool URL or name |
| `--gpus` | all | Comma-separated GPU IDs |
| `--wallet` | required | PRL wallet address |
| `--worker` | pearlvolt | Worker name |

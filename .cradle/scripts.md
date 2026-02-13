# Scripts

| Name | Command | Description |
|------|---------|-------------|
| `stylus:build` | `cd contracts/mycontract && cargo build --release --target wasm32-unknown-unknown` |  |
| `stylus:check` | `cd contracts/mycontract && cargo stylus check` |  |
| `deploy:sepolia` | `bash scripts/deploy-sepolia.sh` |  |
| `deploy:mainnet` | `bash scripts/deploy-mainnet.sh` |  |
| `lint` | `biome lint .` | Run linter |
| `lint:fix` | `biome lint --write .` | Fix lint errors |
| `format` | `biome format --write .` | Format code |
| `format:check` | `biome format .` | Check formatting |
| `test` | `vitest run` | Run tests |
| `test:coverage` | `vitest run --coverage` | Run tests with coverage |
| `typecheck` | `tsc --noEmit` | Run type checker |
| `prepare` | `husky` | Set up git hooks |
| `security:install` | `bash scripts/install-radar.sh` |  |
| `security:analyze` | `bash scripts/run-radar.sh` |  |
| `deploy:sepolia` | `bash scripts/deploy-sepolia.sh` |  |
| `deploy:mainnet` | `bash scripts/deploy-mainnet.sh` |  |
| `fix-scripts` | `command -v dos2unix >/dev/null && dos2unix scripts/*.sh 2>/dev/null || echo "Run: dos2unix scripts/*.sh (install: apt install dos2unix / brew install dos2unix)"` |  |

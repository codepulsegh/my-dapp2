# Integration Map

How components connect and what data flows between them.

### Stylus-rust-contract --> Repo-quality-gates

- **Source**: Stylus-rust-contract (`f15e8607`)
  - Output ports: Contract Code (contract)
- **Target**: Repo-quality-gates (`3633f08d`)
  

### Repo-quality-gates --> Auditware-analyzing

- **Source**: Repo-quality-gates (`3633f08d`)
  - Output ports: Quality Config (config)
- **Target**: Auditware-analyzing (`270ee821`)
  - Input ports: Contract Input (contract)

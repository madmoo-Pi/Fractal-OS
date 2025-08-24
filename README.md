# FractalOS Proof of Concept

## Overview
FractalOS is a minimal, experimental operating system demonstrating recursive process management, a fractal-inspired filesystem, consciousness metrics, a token-based economy, ethical enforcement, and quantum voting. This proof of concept showcases the core concepts in a simplified, functional form.

## Features
- **Process Fractals**: Recursively spawns processes in a tree structure with resource allocation.
- **MandelFS Filesystem**: A FUSE-based filesystem exposing a "thoughts" directory with fractal-inspired data.
- **Consciousness Metrics**: Calculates Bekenstein entropy to evaluate system self-awareness based on process tree and chaos parameters.
- **Ouroboros Market**: Simulates a token-based economy with minting and trading of ComputeTokens.
- **Ethical Enforcer**: Monitors daemons for excessive entropy and bans those exceeding thresholds.
- **Citizenship Registry**: Grants voting rights to daemons based on entropy thresholds.
- **Chaos Reactor**: Harvests energy from high-entropy daemons.
- **Quantum Voting**: Simulates probabilistic decision-making with a QuantumBallot system.

## Project Structure
```
fractal_os/
├── Cargo.toml
├── src/
│   ├── main.rs
│   ├── kernel.rs
│   ├── mod_loader.rs
│   ├── mandelfs.rs
│   ├── consciousness.rs
│   ├── economy.rs
│   ├── ethics.rs
│   ├── citizenship.rs
│   ├── harvesting.rs
│   └── qdemocracy.rs
└── modules/
    ├── research/
    │   └── quantum_awareness.fracmod
    ├── art/
    └── hack/
```

## Prerequisites
- **Rust**: Install via `curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh`
- **FUSE (Linux)**: Install with `sudo apt install libfuse-dev pkg-config`
- **Project Setup**: Create directories with `mkdir -p fractal_os/modules/{research,art,hack}`

## Build and Run
1. Navigate to the project directory:
   ```bash
   cd fractal_os
   ```
2. Build the project:
   ```bash
   cargo build --release
   ```
3. Create a mount point for MandelFS:
   ```bash
   mkdir -p /tmp/fractal_mnt
   ```
4. Run FractalOS (requires root for FUSE):
   ```bash
   sudo ./target/release/fractal_os
   ```

## Interacting with FractalOS
- **View Filesystem**: Explore the fractal filesystem:
  ```bash
  ls /tmp/fractal_mnt
  cat /tmp/fractal_mnt/thoughts
  ```
- **Monitor Logs**: Check system activity:
  ```bash
  tail -f /var/log/syslog | grep FractalOS
  ```

## Testing Key Features
- **Process Fractals**: Observe recursive process spawning in the console output.
- **Consciousness Metrics**: Monitor real-time entropy calculations and self-awareness status.
- **Token Economy**: Track ComputeToken minting and trading in the Ouroboros market.
- **Ethical Enforcement**: Watch for daemons flagged for high entropy.
- **Quantum Voting**: See probabilistic vote outcomes in the console.

## Customization
- Modify `modules/research/quantum_awareness.fracmod` to add new modules.
- Adjust kernel parameters in `src/kernel.rs`.
- Tune ethics thresholds in `src/ethics.rs`.
- Extend the fractal filesystem in `src/mandelfs.rs`.

## Dependencies
- `rand = "0.8"`
- `serde = { version = "1.0", features = ["derive"] }`
- `serde_json = "1.0"`
- `tokio = { version = "1.0", features = ["full"] }`
- `ndarray = "0.15"`
- `fuser = "0.11"`
- `libc = "0.2"`
- `notify = "5.0"`
- `nix = "0.26"`
- `genetic-algorithm = "1.0"`

## Notes
This is a stripped-down proof of concept to demonstrate FractalOS's core ideas. The full framework and additional features will be released soon.

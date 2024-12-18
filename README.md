# Groth16 Installation and Usage Guide

## CUDA Backend Installation

1. **Download the Release Binaries**
   - Download the latest release binaries from the [ICICLE Releases](https://github.com/ingonyama-zk/icicle/releases/).

2. **Install the Binaries**
   - Extract the downloaded binaries to a directory

3. **Set the Installation Path**
   - Set the `ICICLE_BACKEND_INSTALL_DIR` environment variable to the installation path:

### Running Groth16

1. **Run on CUDA Device**
   ```bash
   LD_LIBRARY_PATH=./lib ./groth16 --device CUDA
   ```

2. **Run on CPU**
   ```bash
   LD_LIBRARY_PATH=./lib ./groth16 --device CPU
   ```

### Executing Proofs

To execute a proof, specify the paths for the witness file, zkey file, and the output paths for the proof and public JSONs.

Example:
```bash
prove --witness ./witness.wtns --zkey ./circuit.zkey --proof ./proof.json --public ./public.json
```
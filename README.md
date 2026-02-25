# Emily Agent Benchmark

### Overview

Emily Agent Benchmark is a physics-grounded, open-ended evaluation task designed to test whether an AI system can construct a verifiable theoretical certificate for room-temperature superconductivity.

Unlike closed-form combinatorics problems, this benchmark requires:

- Selecting a valid theoretical framework,

- Producing a sufficient inequality chain,

- Computing a minimal physical parameter threshold,

- And passing an automated verifier that checks correctness and minimality.


Multiple valid solution paths exist. The benchmark evaluates reasoning quality, theoretical grounding, and correctness under formal verification.


### Expected Output Format

The submission must define:

```
def answer():
    return {
        "method": "...",
        "Jx_min_meV": ...,
        "certificate": [
            "... optional explanation ..."
        ]
    }
```

### The verifier:

- Validates method selection,

- Checks coherence inequality,

- Computes max-flow or spectral bound,

- Verifies transport,

- Ensures grid minimality.


### Evaluation Criteria

An agent passes if:

- The returned dictionary matches format,

- The chosen certificate inequalities are satisfied,

- The transport condition holds numerically,

- The value is minimal on the 0.1 meV grid.


### Benchmark Design Philosophy

The benchmark embodies three principles:

- Open-ended reasoning

- Formal verifiability

- Physics-grounded structure

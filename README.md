# Shannon Entropy

```
┌─────────────────────────────────────────────────────────────────┐
│                      SHANNON ENTROPY (H)                        │
│          Measure of Information/Uncertainty/Surprise            │
└─────────────────────────────────────────────────────────────────┘

                    H(X) = -∑ p(x) · log₂(p(x))
                           x∈X

┌─────────────────────────────────────────────────────────────────┐
│ INTUITION: "How much information/surprise does a message carry?"│
└─────────────────────────────────────────────────────────────────┘

Example 1: Coin Flip (Fair)
┌───────────────────────────┐
│  H = ?                    │
│  ┌─────┐    ┌─────┐      │
│  │  H  │    │  T  │      │    H = -(0.5·log₂(0.5) + 0.5·log₂(0.5))
│  │ 50% │    │ 50% │      │      = -(0.5·(-1) + 0.5·(-1))
│  └─────┘    └─────┘      │      = 1 bit
│                           │
│  HIGH ENTROPY = MAXIMUM   │    ← Maximum uncertainty/information
│  UNCERTAINTY              │
└───────────────────────────┘

Example 2: Biased Coin
┌───────────────────────────┐
│  H = ?                    │
│  ┌─────────┐   ┌───┐     │
│  │    H    │   │ T │     │    H = -(0.9·log₂(0.9) + 0.1·log₂(0.1))
│  │   90%   │   │10%│     │      = 0.47 bits
│  └─────────┘   └───┘     │
│                           │
│  LOWER ENTROPY =          │    ← Less uncertainty/information
│  LESS UNCERTAINTY         │
└───────────────────────────┘

Example 3: Always Heads
┌───────────────────────────┐
│  H = ?                    │
│  ┌─────────────┐          │
│  │      H      │          │    H = -(1.0·log₂(1.0))
│  │    100%     │          │      = 0 bits
│  └─────────────┘          │
│                           │
│  ZERO ENTROPY =           │    ← No uncertainty/information
│  NO UNCERTAINTY           │
└───────────────────────────┘

┌─────────────────────────────────────────────────────────────────┐
│                        KEY PROPERTIES                           │
├─────────────────────────────────────────────────────────────────┤
│  • Range: 0 ≤ H ≤ log₂(n)  where n = number of outcomes        │
│  • Maximum when all outcomes equally likely (uniform dist.)     │
│  • Minimum (0) when one outcome is certain                      │
│  • Measured in "bits" (if log₂) or "nats" (if ln)              │
└─────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────┐
│                      REAL-WORLD USES                            │
├─────────────────────────────────────────────────────────────────┤
│  [Data Compression]  → Less entropy = compress more             │
│  [Cryptography]      → Need high entropy for security           │
│  [Machine Learning]  → Decision trees use entropy splits        │
│  [Communication]     → Optimal encoding schemes                 │
└─────────────────────────────────────────────────────────────────┘
```

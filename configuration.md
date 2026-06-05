# ─────────────────────────────────────────────────────────────────────────────
# USER CONFIGURATION  ← edit this section to define your experiments
# ─────────────────────────────────────────────────────────────────────────────
RUNS = [
    {
        "label":         "baseline (sigmoid, 32 neurons)",
        "hidden_layers": [64]
        "learning_rate": 0.05,
        "epochs":        1000,
        "lr_decay":      0.9995,          # no decay
        "activation":    "sigmoid",
    },
    {
        "label":         "ReLU, lr decay",
        "hidden_layers": [64],
        "learning_rate": 0.05,
        "epochs":        1000,
        "lr_decay":      0.9995,        # gentle exponential decay
        "activation":    "relu",
    },
    {
        "label":         "tanh, more neurons",
        "hidden_layers": [64],
        "learning_rate": 0.05,
        "epochs":        1000,
        "lr_decay":      0.9995,
        "activation":    "tanh",
    },
    {
        "label":         "leaky ReLU, small net",
        "hidden_layers": [64],
        "learning_rate": 0.05,
        "epochs":        1000,
        "lr_decay":      0.9995,
        "activation":    "leaky_relu",
    },
]
# ─────────────────────────────────────────────────────────────────────────────

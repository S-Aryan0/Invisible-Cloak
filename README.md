# Invisibility Cloak with OpenCV

This project recreates the famous "Invisibility Cloak" effect (inspired by Harry Potter) using **Python** and **OpenCV**.

The program detects a specific color (in this case, red) in real-time and replaces it with the previously captured background — making it appear as if the cloak (and the person wearing it) has vanished.

---

## How It Works

### 1. Capture Background

The program records a few frames at the start (without the user in view) to set a clean background reference.

```python
for i in range(60):
    ret, background = cap.read()
    background = np.flip(background, axis=1)
```

---



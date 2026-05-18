# 🚀 HydroControl — Autonomous Hydroponic Regulation System

> **Intelligent embedded AI control (Gemma4 via Ollama) with real-time visualization and actuator control.**

---

## 📺 Presentation & Demo

- 🎥 **Link to demo video**: (https://youtu.be/hNN2RKYygBE)

### User Interface Preview

![Control Interface](./Capture%20d'écran%202026-05-18%20130101.png)

| Parameter     | Current Value | Target      | Quick Actions                                       |
|---------------|----------------|-------------|-----------------------------------------------------|
| pH            | 6.1            | 5.8 – 6.2   | –1.0 / –0.5 / –0.2 / +0.2 / +0.5 / +1.0            |
| Temperature   | 21.0 °C        | 20 – 22 °C  | –3°C / –2°C / –1°C / +1°C / +2°C / +3°C            |
| Conductivity  | 2.4 mS/cm      | 1.5 – 2.5   | –1.0 / –0.5 / –0.2 / +0.2 / +0.5 / +1.0            |

### Node-RED Flow Architecture

![Node-RED Flow](./Capture%20d'écran%202026-05-18%20125812.png)

1. Inject (3s) → 2. Get measurements → 3. Prepare prompt → 4. Ollama (Gemma4) → 5. Parse → 6. Execute action → 7. Send to UI → 8. Endpoint `/hydrocontrol/set`

---

## 📂 Deliverables

### 📄 Research Report (PDF/LaTeX)
📥 **[Download Report](./Rapport.zip)**

### ⚙️ Backend Node-RED
📂 **`Hack.json`** (import file)

> ⚠️ The interface does **not** use `node-red-dashboard` but a standalone `ui_template`.

---

## 🛠️ Deployment

1. **Clone or download** this repository.
2. **Import** `Hack.json` into Node-RED (Menu → Import).
3. **Configure Ollama**:  
   - Default URL: `http://host.docker.internal:11434/api/generate`  
   - Required model: `gemma4` (pull it with `ollama pull gemma4`)
4. **Deploy** and access the **HydroControl — Gemma4** tab at `http://<your-ip>:1880/`.

## 🧪 Degraded Mode (without Ollama)

A local deterministic simulation automatically takes over.

---

## 👤 Author

**Habibena Rayane** – Hackathon May 18, 2026 
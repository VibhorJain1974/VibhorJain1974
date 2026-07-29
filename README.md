<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f2027,50:203a43,100:2c5364&height=200&section=header&text=Vibbhor%20Jain&fontSize=70&fontColor=ffffff&animation=fadeIn&fontAlignY=35&desc=Backend%20%C2%B7%20ML%20%C2%B7%20Systems%20that%20reach%20people%20without%20smartphones&descAlignY=55&descSize=16" width="100%"/>

</div>

```
██╗   ██╗██╗██████╗ ██████╗ ██╗  ██╗ ██████╗ ██████╗
██║   ██║██║██╔══██╗██╔══██╗██║  ██║██╔═══██╗██╔══██╗
██║   ██║██║██████╔╝██████╔╝███████║██║   ██║██████╔╝
╚██╗ ██╔╝██║██╔══██╗██╔══██╗██╔══██║██║   ██║██╔══██╗
 ╚████╔╝ ██║██████╔╝██████╔╝██║  ██║╚██████╔╝██║  ██║
  ╚═══╝  ╚═╝╚═════╝ ╚═════╝ ╚═╝  ╚═╝ ╚═════╝ ╚═╝  ╚═╝
     ██╗ █████╗ ██╗███╗   ██╗
     ██║██╔══██╗██║████╗  ██║
     ██║███████║██║██╔██╗ ██║
██   ██║██╔══██║██║██║╚██╗██║
╚█████╔╝██║  ██║██║██║ ╚████║
 ╚════╝ ╚═╝  ╚═╝╚═╝╚═╝  ╚═══╝
```

<div align="center">

<img src="https://readme-typing-svg.herokuapp.com?font=JetBrains+Mono&weight=600&size=22&duration=3000&pause=800&color=00D9FF&center=true&vCenter=true&width=700&lines=Third-year+AI+%26+ML+student+%40+VIPS-TC%2C+Delhi;I+build+for+bad+hardware+and+worse+internet;My+storm+alert+system+calls+farmers+on+feature+phones;%2370+%2F+1%2C773+%E2%80%94+HackerRank+Orchestrate+2026" alt="Typing SVG" />

<br/>

[![Profile Views](https://komarev.com/ghpvc/?username=VibhorJain1974&label=Profile%20Views&color=00d9ff&style=for-the-badge)](https://github.com/VibhorJain1974)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/vibbhor-jain)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:jainvibbhor@gmail.com)

</div>

---

## 🛰️ whoami

```yaml
name:      Vibbhor Jain
role:      Third-year B.Tech, AI & Machine Learning
where:     VIPS-TC, GGSIPU — New Delhi, India
focus:     [ backend, applied ML, systems for constrained devices ]
building:  KAVACH — space weather alerts via Hindi voice calls
thesis:    "the constraint is the device, not the model"
status:    open to software / ML engineering internships
```

The problem I keep coming back to isn't whether a model can do something. It's whether the result can reach a person on a 2G connection holding a phone that doesn't run apps. That's why KAVACH is a **phone call** and not a dashboard, and why Helix runs entirely **in the browser** with no server.

---

## ⚡ What I've shipped

<details open>
<summary><b>🛰️ KAVACH — Autonomous Space Weather Shield</b> &nbsp;<code>LIVE</code></summary>

<br/>

> The May 2024 geomagnetic storm was the strongest in 20 years. India's grid utilities got **zero** automated warning.

```
NASA DONKI  ──┐
              ├──▶  severity classifier  ──▶  28 DISCOM zones  ──▶  ☎️  Hindi voice call
NOAA SWPC   ──┘         (autonomous)            (lat/lng map)         (feature phone)
```

- Polls NASA DONKI every 15 min, NOAA SWPC every 5 min — **zero human trigger**
- Twilio Programmable Voice + Amazon Polly `hi-IN` → calls basic feature phones. No app. No internet.
- 13-endpoint FastAPI backend with SSE streaming; full storm replay renders in **22.6s**
- Backtested on 4 historical storms (2003–2024): 847 simulated alerts, ~6 hr mean lead time

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white)
![Twilio](https://img.shields.io/badge/Twilio-F22F46?style=flat-square&logo=twilio&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white)
![Railway](https://img.shields.io/badge/Railway-0B0D0E?style=flat-square&logo=railway&logoColor=white)

**[→ repo](https://github.com/VibhorJain1974/kavach-faraway-2026)**

</details>

<details>
<summary><b>🏙️ Urban-GenX — Privacy-Preserving Synthetic City Digital Twin</b></summary>

<br/>

> Most "private" ML claims are never tested. So I attacked my own model.

- DP-SGD on a cGAN discriminator at **ε ≤ 10.0, δ = 1e-5** via RDP accountant
- Ran a shadow-model **membership inference attack** against my own weights → **AUC ≈ 0.54**, statistically a coin flip
- Federated across 2 Flower clients over 5 FedAvg rounds, Dockerised, 8-check sanity suite
- SBERT natural-language interface mapping free text → 8 urban scene presets

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)

**[→ repo](https://github.com/VibhorJain1974/Urban-GenX)**

</details>

<details>
<summary><b>📸 Memoria — Full-Stack Photo Platform</b> &nbsp;<code>LIVE</code></summary>

<br/>

- SSR auth via `@supabase/ssr`, admin/member/viewer RBAC enforced per group, invite-code join flow
- **Direct-to-R2 presigned uploads** — media never touches the database tier, served via CDN
- 4-table Postgres schema supporting photo, video, live-photo and boomerang types
- Scoped, built, debugged and deployed solo, end to end

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare_R2-F38020?style=flat-square&logo=cloudflare&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)

**[→ live](https://memoria-gamma-ten.vercel.app)** · **[→ repo](https://github.com/VibhorJain1974/memoria)**

</details>

<details>
<summary><b>🌾 Crop Radar — GNN Climate Risk Intelligence</b></summary>

<br/>

- **LightGCN written in plain PyTorch** — no torch_geometric — over a 30-zone adjacency graph
- 5-class agricultural risk classification across Indian farming regions
- Live ingestion from Open-Meteo Archive + SoilGrids v2, synthetic fallback for offline runs
- SHAP KernelExplainer panel so predictions are explainable, not just accurate

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)

**[→ repo](https://github.com/VibhorJain1974/crop_radar)**

</details>

<details>
<summary><b>🧬 Helix — Offline-First Healthcare Toolkit</b></summary>

<br/>

> Zero server. Zero install. Loads from one URL, then works with the network off.

- **VERA** — skin-lesion classification, TF.js + WebGL, 4s inference
- **VERUM** — counterfeit-drug detection via CIELab + DCT analysis
- **ASCEND** — WebGPU compute shaders + WebRTC mesh
- pnpm monorepo, all inference on-device — no data leaves the phone

![TensorFlow](https://img.shields.io/badge/TensorFlow.js-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![WebGPU](https://img.shields.io/badge/WebGPU-005A9C?style=flat-square&logo=webgl&logoColor=white)

**[→ repo](https://github.com/VibhorJain1974/Helix)**

</details>

---

## 🧰 Toolbox

<div align="center">

<img src="https://skillicons.dev/icons?i=python,typescript,javascript,java,cpp,fastapi,nextjs,react,nodejs,tailwind&theme=dark" />
<br/>
<img src="https://skillicons.dev/icons?i=pytorch,tensorflow,postgres,supabase,mongodb,docker,git,vercel,linux,vscode&theme=dark" />

</div>

---

## 📊 The numbers

<div align="center">

<img height="165" src="https://github-readme-stats.vercel.app/api?username=VibhorJain1974&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=00D9FF&icon_color=00D9FF&count_private=true&include_all_commits=true" />
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=VibhorJain1974&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=00D9FF&langs_count=8" />

<br/>

<img src="https://github-readme-streak-stats.herokuapp.com/?user=VibhorJain1974&theme=tokyonight&hide_border=true&background=0D1117&ring=00D9FF&fire=00D9FF&currStreakLabel=00D9FF" />

<br/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=VibhorJain1974&theme=tokyo-night&hide_border=true&bg_color=0D1117&color=00D9FF&line=00D9FF&point=FFFFFF&area=true" width="100%" />

</div>

---

## 🐍 Watch the snake eat my commits

<div align="center">

![Snake animation](https://raw.githubusercontent.com/VibhorJain1974/VibhorJain1974/output/snake.svg)

</div>

---

## 🏆 Track record

<div align="center">

| | |
|---|---|
| 🥇 | **#70 / 1,773** — HackerRank Orchestrate, June 2026 · Agentic AI Build |
| 🥈 | **#246 / 12,885** across 48 countries — Orchestrate, May 2026 |
| 🎯 | **Top 10 / 200+ teams** — Hackaccino 4.0, Bennett University |
| 👥 | **Operations Head**, Aarvak Tech Society — Gen AI bootcamp, 100+ participants |

<br/>

<img src="https://github-profile-trophy.vercel.app/?username=VibhorJain1974&theme=tokyonight&no-frame=true&no-bg=true&column=7&margin-w=8" width="100%" />

</div>

---

<div align="center">

### 💬 Reach me

[![Email](https://img.shields.io/badge/jainvibbhor@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:jainvibbhor@gmail.com)
[![LinkedIn](https://img.shields.io/badge/vibbhor--jain-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/vibbhor-jain)

<br/>

<i>Open to software and ML engineering internships · Delhi NCR / Remote</i>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2c5364,50:203a43,100:0f2027&height=120&section=footer" width="100%"/>

</div>

<div align="center">

<img src="https://raw.githubusercontent.com/VibhorJain1974/VibhorJain1974/main/assets/hero-banner.svg" width="100%" alt="Vibbhor Jain — Backend · Applied ML"/>

<br/><br/>

[![Email](https://img.shields.io/badge/jainvibbhor@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:jainvibbhor@gmail.com)
[![LinkedIn](https://img.shields.io/badge/vibbhor--jain-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/vibbhor-jain)
[![Profile Views](https://komarev.com/ghpvc/?username=VibhorJain1974&label=VISITORS&color=00e5ff&style=for-the-badge)](https://github.com/VibhorJain1974)

</div>

---

## whoami

```yaml
name:      Vibbhor Jain
role:      Third-year B.Tech, AI & Machine Learning
where:     VIPS-TC, GGSIPU — New Delhi, India
focus:     [ backend, applied ML, systems for constrained devices ]
shipping:  KAVACH — space weather alerts via Hindi voice calls
status:    open to software / ML engineering internships
```

The question I keep coming back to isn't whether a model can do something. It's whether the result can reach a person on a 2G connection holding a phone that doesn't run apps.

That's why KAVACH is a **phone call** and not a dashboard, and why Helix runs entirely **in the browser** with no server behind it.

---

## KAVACH — how it actually works

<div align="center">

<img src="https://raw.githubusercontent.com/VibhorJain1974/VibhorJain1974/main/assets/kavach-pipeline.svg" width="100%" alt="KAVACH alert pipeline"/>

</div>

> The May 2024 geomagnetic storm was the strongest in 20 years. India's grid utilities got **zero** automated warning.

- Polls **NASA DONKI** every 15 min and **NOAA SWPC** every 5 min — no human trigger anywhere in the loop
- Classifies storm severity and maps risk onto **28 Indian DISCOM grid zones** by lat/lng
- Delivers via **Twilio Programmable Voice + Amazon Polly `hi-IN`** — Hindi calls to basic feature phones. No app. No internet. No smartphone.
- **13-endpoint FastAPI backend** with SSE streaming; full storm replay renders in **22.6s**
- Backtested on 4 historical storms (2003–2024): 847 simulated alerts, ~6 hr mean lead time

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white)
![Twilio](https://img.shields.io/badge/Twilio-F22F46?style=flat-square&logo=twilio&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white)
![Railway](https://img.shields.io/badge/Railway-0B0D0E?style=flat-square&logo=railway&logoColor=white)

**[→ repository](https://github.com/VibhorJain1974/kavach-faraway-2026)**

---

## Everything else I've built

<details>
<summary><b>Urban-GenX — Privacy-Preserving Synthetic City Digital Twin</b></summary>

<br/>

> Most "private" ML claims are never tested. So I attacked my own model.

- DP-SGD on a cGAN discriminator at **ε ≤ 10.0, δ = 1e-5** via RDP accountant
- Ran a shadow-model **membership inference attack** against my own weights → **AUC ≈ 0.54**, statistically a coin flip
- Federated across 2 Flower clients over 5 FedAvg rounds, Dockerised, 8-check sanity suite
- SBERT natural-language interface mapping free text to 8 urban scene presets

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)

**[→ repository](https://github.com/VibhorJain1974/Urban-GenX)**

</details>

<details>
<summary><b>Memoria — Full-Stack Photo Platform</b> · <code>LIVE</code></summary>

<br/>

- SSR auth via `@supabase/ssr` with admin/member/viewer RBAC enforced per group, invite-code join flow
- **Direct-to-R2 presigned uploads** — media never touches the database tier, served over CDN
- 4-table Postgres schema supporting photo, video, live-photo and boomerang types
- Scoped, built, debugged and deployed solo, end to end

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare_R2-F38020?style=flat-square&logo=cloudflare&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)

**[→ live](https://memoria-gamma-ten.vercel.app)** · **[→ repository](https://github.com/VibhorJain1974/memoria)**

</details>

<details>
<summary><b>Crop Radar — GNN Climate Risk Intelligence</b></summary>

<br/>

- **LightGCN written in plain PyTorch** — no torch_geometric — over a 30-zone adjacency graph
- 5-class agricultural risk classification across Indian farming regions
- Live ingestion from Open-Meteo Archive + SoilGrids v2, synthetic fallback for offline runs
- SHAP KernelExplainer panel so predictions are explainable, not just accurate

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)

**[→ repository](https://github.com/VibhorJain1974/crop_radar)**

</details>

<details>
<summary><b>Helix — Offline-First Healthcare Toolkit</b></summary>

<br/>

> Zero server. Zero install. Loads from one URL, then works with the network off.

- **VERA** — skin-lesion classification, TF.js + WebGL, 4s inference
- **VERUM** — counterfeit-drug detection via CIELab + DCT analysis
- **ASCEND** — WebGPU compute shaders + WebRTC mesh
- pnpm monorepo, all inference on-device — no data leaves the phone

![TensorFlow](https://img.shields.io/badge/TensorFlow.js-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![WebGPU](https://img.shields.io/badge/WebGPU-005A9C?style=flat-square&logo=webgl&logoColor=white)

**[→ repository](https://github.com/VibhorJain1974/Helix)**

</details>

---

## Toolbox

<div align="center">

<img src="https://skillicons.dev/icons?i=python,typescript,javascript,java,cpp,fastapi,nextjs,react,nodejs,tailwind&theme=dark" />
<br/>
<img src="https://skillicons.dev/icons?i=pytorch,tensorflow,postgres,supabase,mongodb,docker,git,vercel,linux,vscode&theme=dark" />

</div>

---

## Activity

<div align="center">

<img height="160" src="https://github-readme-stats.vercel.app/api/top-langs/?username=VibhorJain1974&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=00E5FF&langs_count=8&cache_seconds=86400" />

<br/><br/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=VibhorJain1974&theme=tokyo-night&hide_border=true&bg_color=0D1117&color=00E5FF&line=00E5FF&point=FFFFFF&area=true" width="100%" />

</div>

---

<div align="center">

<sub>Open to software and ML engineering internships · Delhi NCR / Remote</sub>

</div>

<div align="center">

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

`backend` · `applied ML` · `systems for constrained devices`

</div>

```yaml
name:       Vibbhor Jain
role:       Third-year B.Tech, AI & Machine Learning
university: VIPS-TC, GGSIPU — New Delhi
cgpa:       7.8 / 10
shipping:   KAVACH — space weather alerts via Hindi voice calls
status:     open to software / ML engineering internships
```

> **The question isn't whether a model can do something.**
> It's whether the result can reach a person on a 2G connection holding a phone that doesn't run apps.
>
> That's why KAVACH is a phone call and not a dashboard, and why Helix runs entirely in the browser with no server.

---

## KAVACH — the pipeline, live

```mermaid
%%{init: {'theme':'base','themeVariables':{
 'primaryColor':'#0d1117','primaryTextColor':'#e6edf3','primaryBorderColor':'#00d9ff',
 'lineColor':'#7b2fff','secondaryColor':'#161b22','tertiaryColor':'#161b22',
 'fontFamily':'ui-monospace, monospace','fontSize':'14px'}}}%%
flowchart LR
  A([NASA DONKI<br/>15 min poll]):::src
  B([NOAA SWPC<br/>5 min poll]):::src
  C{{severity<br/>classifier}}:::brain
  D[[28 DISCOM zones<br/>lat/lng risk map]]:::zone
  E[/FastAPI<br/>13 endpoints · SSE/]:::api
  F(("Twilio +<br/>Polly hi-IN")):::voice
  G([feature phone<br/>no app · no internet]):::phone

  A --> C
  B --> C
  C -->|Kp index| D
  D --> E
  E -->|storm detected| F
  F ==>|Hindi voice call| G

  classDef src fill:#0d1117,stroke:#ff9500,stroke-width:2px,color:#ffb84d
  classDef brain fill:#1a0d2e,stroke:#7b2fff,stroke-width:2px,color:#c9a3ff
  classDef zone fill:#0d1117,stroke:#00d9ff,stroke-width:2px,color:#7fe7ff
  classDef api fill:#0d1117,stroke:#00ff9c,stroke-width:2px,color:#6affc4
  classDef voice fill:#2e0d1f,stroke:#ff2d95,stroke-width:3px,color:#ff8ac4
  classDef phone fill:#0d1117,stroke:#00ff9c,stroke-width:3px,color:#6affc4
```

### the zones it calls — drag to pan, scroll to zoom

```geojson
{
 "type": "FeatureCollection",
 "features": [
  {
   "type": "Feature",
   "properties": {
    "name": "Delhi \u2014 severe risk",
    "marker-color": "#ff2d95",
    "marker-size": "medium",
    "marker-symbol": "triangle"
   },
   "geometry": {
    "type": "Point",
    "coordinates": [
     77.21,
     28.61
    ]
   }
  },
  {
   "type": "Feature",
   "properties": {
    "name": "Jaipur \u2014 high risk",
    "marker-color": "#ff9500",
    "marker-size": "medium",
    "marker-symbol": "triangle"
   },
   "geometry": {
    "type": "Point",
    "coordinates": [
     75.79,
     26.91
    ]
   }
  },
  {
   "type": "Feature",
   "properties": {
    "name": "Lucknow \u2014 high risk",
    "marker-color": "#ff9500",
    "marker-size": "medium",
    "marker-symbol": "triangle"
   },
   "geometry": {
    "type": "Point",
    "coordinates": [
     80.95,
     26.85
    ]
   }
  },
  {
   "type": "Feature",
   "properties": {
    "name": "Patna \u2014 moderate risk",
    "marker-color": "#ffd60a",
    "marker-size": "medium",
    "marker-symbol": "triangle"
   },
   "geometry": {
    "type": "Point",
    "coordinates": [
     85.14,
     25.59
    ]
   }
  },
  {
   "type": "Feature",
   "properties": {
    "name": "Kolkata \u2014 moderate risk",
    "marker-color": "#ffd60a",
    "marker-size": "medium",
    "marker-symbol": "triangle"
   },
   "geometry": {
    "type": "Point",
    "coordinates": [
     88.36,
     22.57
    ]
   }
  },
  {
   "type": "Feature",
   "properties": {
    "name": "Guwahati \u2014 low risk",
    "marker-color": "#00ff9c",
    "marker-size": "medium",
    "marker-symbol": "triangle"
   },
   "geometry": {
    "type": "Point",
    "coordinates": [
     91.74,
     26.14
    ]
   }
  },
  {
   "type": "Feature",
   "properties": {
    "name": "Bhopal \u2014 high risk",
    "marker-color": "#ff9500",
    "marker-size": "medium",
    "marker-symbol": "triangle"
   },
   "geometry": {
    "type": "Point",
    "coordinates": [
     77.41,
     23.26
    ]
   }
  },
  {
   "type": "Feature",
   "properties": {
    "name": "Ahmedabad \u2014 severe risk",
    "marker-color": "#ff2d95",
    "marker-size": "medium",
    "marker-symbol": "triangle"
   },
   "geometry": {
    "type": "Point",
    "coordinates": [
     72.57,
     23.02
    ]
   }
  },
  {
   "type": "Feature",
   "properties": {
    "name": "Mumbai \u2014 moderate risk",
    "marker-color": "#ffd60a",
    "marker-size": "medium",
    "marker-symbol": "triangle"
   },
   "geometry": {
    "type": "Point",
    "coordinates": [
     72.88,
     19.08
    ]
   }
  },
  {
   "type": "Feature",
   "properties": {
    "name": "Hyderabad \u2014 low risk",
    "marker-color": "#00ff9c",
    "marker-size": "medium",
    "marker-symbol": "triangle"
   },
   "geometry": {
    "type": "Point",
    "coordinates": [
     78.49,
     17.39
    ]
   }
  },
  {
   "type": "Feature",
   "properties": {
    "name": "Bengaluru \u2014 low risk",
    "marker-color": "#00ff9c",
    "marker-size": "medium",
    "marker-symbol": "triangle"
   },
   "geometry": {
    "type": "Point",
    "coordinates": [
     77.59,
     12.97
    ]
   }
  },
  {
   "type": "Feature",
   "properties": {
    "name": "Chennai \u2014 low risk",
    "marker-color": "#00ff9c",
    "marker-size": "medium",
    "marker-symbol": "triangle"
   },
   "geometry": {
    "type": "Point",
    "coordinates": [
     80.27,
     13.08
    ]
   }
  }
 ]
}
```

```diff
@@  KAVACH · autonomous space weather shield · LIVE · Team 404_SHINOBI  @@

! May 2024 brought the strongest geomagnetic storm in 20 years.
! India's grid utilities got zero automated warning.

+ Hindi voice calls to feature phones. No app. No internet.
+ 13-endpoint FastAPI backend, SSE streaming, 22.6s full storm replay
+ Backtested on 4 storms (2003-2024): 847 alerts, ~6 hr mean lead time
+ Zero human trigger anywhere in the loop

# FastAPI · APScheduler · Next.js 14 · Supabase · Twilio · Railway
# github.com/VibhorJain1974/kavach-faraway-2026
```

---

## everything else — click to open

<details>
<summary><b>URBAN-GENX</b> — privacy-preserving synthetic city digital twin</summary>

```mermaid
%%{init: {'theme':'base','themeVariables':{
 'primaryColor':'#1a0d2e','primaryTextColor':'#e6edf3','primaryBorderColor':'#7b2fff',
 'lineColor':'#00d9ff','fontFamily':'ui-monospace, monospace'}}}%%
flowchart TD
  R[(raw urban data)]:::a --> S[cGAN + Beta-VAE]:::b
  S --> DP[DP-SGD via Opacus<br/>eps &lt;= 10.0 · delta 1e-5]:::c
  DP --> FL[Flower FedAvg<br/>2 clients · 5 rounds]:::d
  FL --> W[[generator weights]]:::e
  W --> AT{{shadow-model<br/>membership inference}}:::f
  AT -->|AUC 0.54| OK([indistinguishable<br/>from random]):::g

  classDef a fill:#0d1117,stroke:#5c7a99,color:#8fb8de
  classDef b fill:#0d1117,stroke:#00d9ff,color:#7fe7ff
  classDef c fill:#1a0d2e,stroke:#7b2fff,stroke-width:3px,color:#c9a3ff
  classDef d fill:#0d1117,stroke:#00d9ff,color:#7fe7ff
  classDef e fill:#0d1117,stroke:#ff9500,color:#ffb84d
  classDef f fill:#2e0d1f,stroke:#ff2d95,stroke-width:2px,color:#ff8ac4
  classDef g fill:#0d2e1f,stroke:#00ff9c,stroke-width:3px,color:#6affc4
```

```diff
+ DP-SGD on a cGAN discriminator at eps <= 10.0, delta = 1e-5 (RDP)
+ Shadow-model membership inference run against my own weights
+ Federated: 2 Flower clients, 5 FedAvg rounds, Docker Compose
+ SBERT natural-language interface over 8 urban scene presets

! Most "private" ML claims are never tested. So I attacked my own model.

# PyTorch · Opacus · Flower · UNet cGAN · Beta-VAE · SBERT
# github.com/VibhorJain1974/Urban-GenX
```

</details>

<details>
<summary><b>MEMORIA</b> — full-stack photo platform · <code>LIVE</code></summary>

```mermaid
%%{init: {'theme':'base','themeVariables':{
 'primaryColor':'#0d1117','primaryTextColor':'#e6edf3','primaryBorderColor':'#00ff9c',
 'lineColor':'#00ff9c','fontFamily':'ui-monospace, monospace'}}}%%
sequenceDiagram
  autonumber
  participant U as browser
  participant N as Next.js 16 (SSR)
  participant S as Supabase
  participant R as Cloudflare R2

  U->>N: upload photo
  N->>S: verify session + group role
  S-->>N: RBAC ok (admin/member/viewer)
  N->>R: request presigned PUT
  R-->>N: signed URL
  N-->>U: signed URL
  U->>R: PUT bytes directly
  Note over U,R: media never touches the DB tier
  U->>N: confirm
  N->>S: insert row + thumbnail
```

```diff
+ SSR auth, admin/member/viewer RBAC enforced per group, invite codes
+ Direct-to-R2 presigned uploads — media never touches the DB tier
+ 4-table Postgres schema: photo, video, live-photo, boomerang
+ Scoped, built, debugged and deployed solo, end to end

# Next.js 16 · TypeScript · Supabase · Cloudflare R2 · Tailwind v4
# memoria-gamma-ten.vercel.app
```

</details>

<details>
<summary><b>CROP RADAR</b> — GNN climate risk across 30 Indian zones</summary>

```diff
+ LightGCN implemented in plain PyTorch. No torch_geometric.
+ 5-class risk classification over a 30-zone adjacency graph
+ SHAP KernelExplainer panel, PyDeck risk map, PDF report export
+ Live Open-Meteo + SoilGrids v2 ingestion, offline synthetic fallback

# Python · PyTorch · LightGCN · SHAP · Streamlit · PyDeck
# github.com/VibhorJain1974/crop_radar
```

</details>

<details>
<summary><b>HELIX</b> — offline-first healthcare toolkit</summary>

```diff
! Zero server. Zero install. One URL, then works with the network off.

+ VERA    skin-lesion classification, TF.js + WebGL, 4s inference
+ VERUM   counterfeit-drug detection via CIELab + DCT analysis
+ ASCEND  WebGPU compute shaders + WebRTC mesh
+ pnpm monorepo, all inference on-device — no data leaves the phone

# TypeScript · TensorFlow.js · WebGL · WebGPU · WebRTC · pnpm
# github.com/VibhorJain1974/Helix
```

</details>

---

## stack

```mermaid
%%{init: {'theme':'base','themeVariables':{
 'pie1':'#00d9ff','pie2':'#7b2fff','pie3':'#ff2d95','pie4':'#00ff9c',
 'pie5':'#ff9500','pie6':'#ffd60a',
 'pieTitleTextSize':'16px','pieSectionTextSize':'13px','pieStrokeWidth':'0px',
 'primaryTextColor':'#0d1117','pieOuterStrokeWidth':'0px',
 'fontFamily':'ui-monospace, monospace'}}}%%
pie showData
  title where the hours go
  "Python / ML" : 34
  "TypeScript / Next.js" : 26
  "FastAPI / backend" : 18
  "Postgres / infra" : 11
  "Java / DSA" : 8
  "everything else" : 3
```

```ini
[languages]  Python · TypeScript · JavaScript · Java · SQL · C/C++ · Bash
[backend]    FastAPI · Node.js · REST APIs · SSE · PostgreSQL · Supabase
[frontend]   Next.js · React · Tailwind CSS · Framer Motion · Radix UI
[ml]         PyTorch · Scikit-learn · XGBoost · SHAP · SBERT · TensorFlow.js
[privacy]    Opacus DP-SGD · Flower FedAvg · differential privacy
[infra]      Docker · Vercel · Railway · Cloudflare R2 · Git
```

---

## track record

```mermaid
%%{init: {'theme':'base','themeVariables':{
 'primaryColor':'#0d1117','primaryTextColor':'#e6edf3','primaryBorderColor':'#00d9ff',
 'lineColor':'#7b2fff','fontFamily':'ui-monospace, monospace',
 'cScale0':'#00d9ff','cScale1':'#7b2fff','cScale2':'#ff2d95'}}}%%
timeline
  title from first hackathon to shipping in production
  Jan 2026 : Gen AI Winter School — directed, 100+ participants
  Mar 2026 : ORBIX Web3 Track — BYLD Hackathon
  Apr 2026 : Hackaccino 4.0 — TOP 10 of 200+ teams
           : Code Royale Hackathon — organised
  May 2026 : HackerRank Orchestrate — #246 of 12,885 · 48 countries
  Jun 2026 : HackerRank Orchestrate — #70 of 1,773
           : KAVACH — idea to live deployment in 6 days
```

```diff
@@  competitions  @@

+ #70 / 1,773        HackerRank Orchestrate · June 2026 · Agentic AI Build
+ #246 / 12,885      HackerRank Orchestrate · May 2026 · 48 countries
+ Top 10 / 200+      Hackaccino 4.0 · Bennett University
+ Round 1 MVP        FAR AWAY 2026 (Zuup) · Team 404_SHINOBI

@@  leadership  @@

+ Operations Head    Aarvak Tech Society, VIPS-TC · 2025-present
+                    Gen AI Winter School — 100+ participants
+                    Code Royale Hackathon — tracks, logistics, mentoring
```

---

```console
$ whois vibbhor

  email      jainvibbhor@gmail.com
  linkedin   linkedin.com/in/vibbhor-jain
  github     github.com/VibhorJain1974
  location   Delhi NCR · open to remote

$ _
```

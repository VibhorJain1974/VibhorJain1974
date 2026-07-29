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

**backend · applied ML · systems for constrained devices**

</div>

```yaml
name:       Vibbhor Jain
role:       Third-year B.Tech, AI & Machine Learning
university: VIPS-TC, GGSIPU — New Delhi, India
cgpa:       7.8 / 10
focus:      [ backend, applied ML, systems for constrained devices ]
shipping:   KAVACH — space weather alerts via Hindi voice calls
status:     open to software / ML engineering internships
contact:    jainvibbhor@gmail.com
```

```console
$ vibbhor --thesis

  The question isn't whether a model can do something.
  It's whether the result can reach a person on a 2G connection
  holding a phone that doesn't run apps.

  That's why KAVACH is a phone call and not a dashboard,
  and why Helix runs entirely in the browser with no server.
```

## builds

```diff
@@  KAVACH · autonomous space weather shield · LIVE · Team 404_SHINOBI  @@

! May 2024 brought the strongest geomagnetic storm in 20 years.
! India's grid utilities got zero automated warning.

    NASA DONKI ─┐
                ├──>  severity model  ──>  28 DISCOM zones  ──>  CALL
    NOAA SWPC  ─┘

+ Hindi voice calls to feature phones. No app. No internet.
+ 13-endpoint FastAPI backend, SSE streaming, 22.6s full storm replay
+ Backtested on 4 storms (2003-2024): 847 alerts, ~6 hr mean lead time
+ Polls DONKI every 15 min, SWPC every 5 min — zero human trigger

# FastAPI · APScheduler · Next.js 14 · Supabase · Twilio · Railway
# github.com/VibhorJain1974/kavach-faraway-2026
```

```diff
@@  URBAN-GENX · privacy-preserving synthetic city digital twin  @@

! Most "private" ML claims are never tested. So I attacked my own model.

+ DP-SGD on a cGAN discriminator at eps <= 10.0, delta = 1e-5 (RDP)
+ Shadow-model membership inference run against my own weights
+     AUC 0.54  ──  statistically a coin flip
+ Federated: 2 Flower clients, 5 FedAvg rounds, Docker Compose
+ SBERT natural-language interface over 8 urban scene presets

# PyTorch · Opacus · Flower · UNet cGAN · Beta-VAE · SBERT · Streamlit
# github.com/VibhorJain1974/Urban-GenX
```

```diff
@@  MEMORIA · full-stack photo platform · LIVE  @@

+ SSR auth, admin/member/viewer RBAC enforced per group, invite codes
+ Direct-to-R2 presigned uploads — media never touches the DB tier
+ 4-table Postgres schema: photo, video, live-photo, boomerang
+ Scoped, built, debugged and deployed solo, end to end

# Next.js 16 · TypeScript · Supabase · Cloudflare R2 · Tailwind v4
# memoria-gamma-ten.vercel.app
```

```diff
@@  CROP RADAR · GNN climate risk across 30 Indian agricultural zones  @@

+ LightGCN implemented in plain PyTorch. No torch_geometric.
+ 5-class risk classification over a 30-zone adjacency graph
+ SHAP KernelExplainer panel, PyDeck risk map, PDF report export
+ Live Open-Meteo + SoilGrids v2 ingestion, offline synthetic fallback

# Python · PyTorch · LightGCN · SHAP · Streamlit · PyDeck
# github.com/VibhorJain1974/crop_radar
```

```diff
@@  HELIX · offline-first healthcare toolkit  @@

! Zero server. Zero install. One URL, then works with the network off.

+ VERA    skin-lesion classification, TF.js + WebGL, 4s inference
+ VERUM   counterfeit-drug detection via CIELab + DCT analysis
+ ASCEND  WebGPU compute shaders + WebRTC mesh
+ pnpm monorepo, all inference on-device — no data leaves the phone

# TypeScript · TensorFlow.js · WebGL · WebGPU · WebRTC · pnpm
# github.com/VibhorJain1974/Helix
```

## stack

```diff
+ Python       ████████████████████░░  92%
+ TypeScript   ███████████████████░░░  86%
+ FastAPI      ███████████████████░░░  88%
+ Next.js      ██████████████████░░░░  84%
+ PyTorch      █████████████████░░░░░  78%
+ PostgreSQL   ████████████████░░░░░░  74%
+ Docker       ███████████████░░░░░░░  68%
+ Java         ██████████████░░░░░░░░  62%
```

```ini
[languages]  Python · TypeScript · JavaScript · Java · SQL · C/C++ · Bash
[backend]    FastAPI · Node.js · REST APIs · SSE · PostgreSQL · Supabase
[frontend]   Next.js · React · Tailwind CSS · Framer Motion · Radix UI
[ml]         PyTorch · Scikit-learn · XGBoost · SHAP · SBERT · TensorFlow.js
[privacy]    Opacus DP-SGD · Flower FedAvg · differential privacy
[infra]      Docker · Vercel · Railway · Cloudflare R2 · Git
```

## track record

```diff
@@  competitions  @@

+ #70 / 1,773        HackerRank Orchestrate · June 2026 · Agentic AI Build
+ #246 / 12,885      HackerRank Orchestrate · May 2026 · 48 countries
+ Top 10 / 200+      Hackaccino 4.0 · Bennett University · Apr 2026
+ Round 1 MVP        FAR AWAY 2026 (Zuup) · Team 404_SHINOBI

@@  leadership  @@

+ Operations Head    Aarvak Tech Society, VIPS-TC · 2025-present
+                    Gen AI Winter School — 100+ participants
+                    Code Royale Hackathon — tracks, logistics, mentoring
```

## contact

```console
$ whois vibbhor

  email      jainvibbhor@gmail.com
  linkedin   linkedin.com/in/vibbhor-jain
  github     github.com/VibhorJain1974
  location   Delhi NCR · open to remote

$ _
```

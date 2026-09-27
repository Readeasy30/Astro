# 🐶 PetNeeds.ai - Cloudflare & GitHub Architecture Tracking Document

## 1. Storage Layer (Cloudflare R2)
- [x] Create R2 Bucket named: `petneeds-media-cache`
- [ ] Ensure public access remains disabled (all traffic proxying through the Worker)

## 2. API Computing Layer (Cloudflare Workers)
- [x] Provision standalone Worker named: `petneeds-avatar-api`
- [x] Configure Variables and Data Bindings in Settings:
  - **Type:** R2 Bucket Binding
  - **Variable Name:** `MEDIA_CACHE`
  - **Bound Bucket:** `petneeds-media-cache`
- [x] Copy & paste production edge-caching script directly into Cloudflare Quick Editor

## 3. Presentation Layer (Cloudflare Pages + Astro)
- [x] Link your GitHub project repository to Cloudflare Pages
- [x] Set Framework Preset: `Astro`
- [x] Confirm clean initial deployment tracking status
- [x] Add inline video streaming canvas components into `src/pages/index.astro`

## 4. Operational Maintenance & Tuning
- [ ] Confirm Worker API target URL matches: `https://workers.dev`
- [ ] Add pre-warming loops to automate asset collection for primary tricks (sit, stay, come)

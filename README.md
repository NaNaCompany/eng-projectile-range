# 경사 투사 도달거리 계산기

같은 높이로 돌아오는 이상적인 포물선 투사 거리 계산

- Plan ID: E062
- App: https://nanalab.kr/eng-projectile-range/
- Repository: https://github.com/NaNaCompany/eng-projectile-range
- Formula: `R = v₀² sin(2θ)/g`
- Output: 동일 높이 수평 도달거리 R

## Model

v₀≥0, g>0, 0≤θ≤90°. 발사점·착지점 높이가 같고 중력이 일정하며 공기저항·양력은 없다. 최대 사거리 최적화나 실제 발사체 설계는 계산하지 않는다.

Inputs are normalized to SI. Only one scalar is returned. Model conditions, finite numbers, physical boundaries, overflow and underflow are checked. External solver APIs and property databases are not used.

## Verification

Run `node --test tests/*.test.mjs` with Node.js 22 or later. Independent 70-digit Decimal example result: `10`. Source and license notices are in [SOURCES.md](SOURCES.md) and [LICENSE](LICENSE).

## Hosting

GitHub Pages uses `main` and `/`, with the NaNaCompany domain inherited. Google GTM, GA4, AdSense, Cloudflare analytics and the gray More Apps link are included. All code, descriptions and graphics are original.

## Static languages

Korean (existing root), English (`en/`), Spanish (`es/`), Simplified Chinese (`zh/`), Japanese (`ja/`) and German (`de/`). Each page has its own canonical URL, reciprocal hreflang, localized metadata, interface, validation messages and preview image. The language links work without JavaScript. Calculation code is shared and no runtime translation API is used.

Edit `localization/*.json` for text, `src/template.html` for the shared page, and run `python scripts/build-locales.py`. Run `python scripts/build-locales.py --check` and `npm test` before publishing. Decimal commas are accepted in Spanish and German; thousands separators are not supported.

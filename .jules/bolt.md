## 2025-05-15 - [Optimize README Image Loading and CDN]
**Learning:** README files with many external assets (like devicons or badges) can suffer from slow load times and main-thread blocking if images are not optimized. Using a fast CDN like `cdn.jsdelivr.net` instead of `raw.githubusercontent.com` provides better delivery. Adding `decoding="async"` prevents the browser from blocking the main thread while decoding images.
**Action:** Always prefer CDNs for assets in markdown and use `decoding="async"` (and `loading="lazy"` for below-the-fold content) to improve perceived performance.

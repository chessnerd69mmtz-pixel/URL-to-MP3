# URL-to-MP3 Converter

A static, browser-based converter intended for GitHub Pages. It can convert a local audio/video file to MP3 with FFmpeg WebAssembly, or fetch a **direct media-file URL** first when the source allows CORS.

## Deploy on GitHub Pages
1. Open **Settings → Pages** in this repository.
2. Under **Build and deployment**, choose **GitHub Actions**.
3. The workflow in `.github/workflows/pages.yml` deploys the static site after a push to `main`.
4. When the workflow succeeds, visit https://chessnerd69mmtz-pixel.github.io/URL-to-MP3/

## Limitations
- A direct URL must point to a media file and the host must allow cross-origin browser requests. Many hosts block this.
- A URL to a webpage, or a streaming platform page, is not a direct media file and cannot be extracted by this static site.
- The first conversion downloads FFmpeg WebAssembly from public CDNs. It needs an internet connection.
- Runtime depends on file size, source codec, device performance, and network speed. No universal 30-second guarantee is possible.
- Processing is in the browser. The fetched media is held in memory, so very large files may fail on low-memory devices.
- Use only files you own or have permission to download and convert. The project does not bypass access controls or platform restrictions.

No API key or server is required.

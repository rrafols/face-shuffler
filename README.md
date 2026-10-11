# Face Shuffle

A one-page mobile web app: it opens the camera, finds the face with
[MediaPipe Face Landmarker](https://ai.google.dev/edge/mediapipe/solutions/vision/face_landmarker)
(on the device), and when you press **SHUFFLE** the eyes, brows, nose and mouth swap places.

- Reset puts the face back, the camera button switches front/back, the arrow saves a PNG.
- Everything is in `index.html`; the library loads from jsDelivr and the model (~4 MB) from Google's storage.

## Run it

Browsers only give the camera to HTTPS pages (or `localhost`), so open it from an HTTPS host:

- **GitHub Pages**: Settings → Pages → deploy from `main`, root. Then open `https://<user>.github.io/face-shuffler/`.
- **Locally**: `npx serve .` (or `python3 -m http.server 8080`) and open `http://localhost:8080` on the same machine.
  For a phone, put an HTTPS tunnel in front, e.g. `cloudflared tunnel --url http://localhost:8080`.

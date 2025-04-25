# 📱 PWA Subtitle Transcriber

A client-side Progressive Web App for recording/uploading video and automatically generating AI-powered subtitles — all on-device, offline-capable.

---

## 🚀 Key Features

- 🎙️ Record or upload video/audio from your mobile device
- 🤖 Run Whisper (OpenAI speech model) **fully client-side**
- ✍️ Generate and export subtitles in `.srt` format
- 🌏 Optional translation using HuggingFace multilingual models
- ⚡ Works offline – no server or API required
- 🧱 Designed to integrate into [`anguskaede`](https://github.com/WhisperLooms/anguskaede) project or other Next.js PWAs

---

## 📂 Project Structure

src/ 
├── app/ │ 
├── camera/ 
│ │ └── page.tsx → Renders the camera module 
│ └── components/ 
│   └── camera/ 
│     ├── Recorder.tsx → Record/upload logic 
│     ├── Transcriber.tsx → Runs Whisper model │ 
├── SubtitleUtils.ts → Generates .srt output 
│ └── Translator.tsx → (Optional) subtitle translator


---

## 🔧 Tech Stack

- Next.js (App Router)
- TypeScript
- Tailwind CSS
- [transformers.js](https://huggingface.co/docs/transformers.js/index)
- `onnxruntime-web`
- PWA enabled with `next-pwa`

---

## 🛠️ Setup

```bash
git clone https://github.com/WhisperLooms/pwa-subtitle-transcriber.git
cd pwa-subtitle-transcriber
pnpm install

# run dev
pnpm dev

pnpm build
pnpm start

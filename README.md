# Affiliate Prompt Generator

A production-grade AI-powered marketing storyboard creator that generates high-fidelity prompts for images, videos, and voiceovers using Google's Gemini API. 

Designed for affiliate marketers, content creators, and social commerce agencies, this tool transforms a product concept and optional visual assets into a cohesive 5-scene ad campaign sequence. It generates natural, organic prompts that bypass common AI visual tropes, fully optimized for the latest generation of media synthesis models.

---

## Key Features

- **5-Step Campaign Pipeline**:
  - **Step 1: Product**: Details product information, category, reference images, and configures the product placeholder toggle.
  - **Step 2: Model**: Configures the protagonist character parameters, reference images, and model placeholder toggle.
  - **Step 3: Background**: Handles setting description, location reference images, and background placeholder toggle.
  - **Step 4: Style & Vibe**: Configures visual style, video vibe, voiceover style, language, aspect ratio, and video hook setting.
  - **Step 5: Results**: Outputs a detailed 5-scene storyboard (Image, Video, Voice) and strategic AI recommendations.

- **Anti-AI Prompting Strategy**: 
  Prompts are designed to bypass the flat, plasticky AI look by avoiding clichés (e.g., "photorealistic", "hyper-realistic") and introducing realistic imperfections such as film grain (Kodak Portra, Vision3), motion blur, dust motes, focus breathing, and casual street photography framing.

- **Synchronized Audio-Video Workflows**:
  Voiceover prompts contain exact foley instructions, pause markers, and an `// AUDIO SYNC NOTE` detailing voice entry, video action correlation, and total segment duration.

- **Multimodal Visual Analysis**:
  Supports uploading multiple product, model, and background images. The Gemini API analyzes colors, textures, lighting, and composition to yield highly context-aware recommendations.

- **Smart Caching & UI Resilience**:
  Users can step back and adjust parameters in the wizard without losing generated storyboard states or unnecessarily consuming API tokens. Fallback mock data allows for evaluation without an API key.

---

## Technical Stack

- **Core Framework**: React 18 (TypeScript)
- **Styling**: Tailwind CSS v3 & PostCSS (Responsive, dark-accented UI)
- **Icons**: Lucide React
- **Build Tooling**: Vite & TypeScript compiler
- **API Client**: Native fetch configuration with exponential backoff retry logic for the Gemini API

---

## Project Structure

```text
Affiliate-Prompt-Generator/
├── src/
│   ├── App.tsx          # Core wizard state, Gemini API execution, and UI markup
│   ├── main.tsx         # Application mount entrypoint
│   └── index.css        # Tailwind directives and custom global design tokens
├── index.html           # Document template
├── tailwind.config.js   # Tailwind CSS configuration
├── postcss.config.js    # PostCSS processor rules
├── tsconfig.json        # Strict TypeScript configuration compiler options
└── README.md            # Technical documentation
```

---

## Getting Started

### Prerequisites

- Node.js (v18.0.0 or higher)
- npm, yarn, or pnpm

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/boncabee/Affiliate-Prompt-Generator.git
   cd Affiliate-Prompt-Generator
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Run the local development server:
   ```bash
   npm run dev
   ```

4. Build the application for production:
   ```bash
   npm run build
   ```
   The build outputs static assets to the `dist/` directory, ready to be served by any static host.

---

## API Configuration & Fallback Mode

1. Acquire a Gemini API Key from the Google AI Studio.
2. Enter the API Key in the configurations panel inside the application. The key is persisted in the browser's `localStorage` and sent directly to Google's API endpoint.
3. If no API key is provided, the application runs in a simulated offline mode, returning an authentic, descriptive mock storyboard to showcase the system features.

---

## Optimized Model Support

The generated outputs are specifically tailored to take advantage of parameters and style configurations in modern models:

### Image Generation
- **Midjourney 6.1** (outputs `--style raw` parameters and utilizes precise aspect ratios)
- **GPT Image 2** (DALL-E 3 architecture)
- **Imagen 4** (Google DeepMind)
- **Nano Banana Pro / 2**

### Video Generation
- **Kling AI 3.0** (supports handheld camera physics, focus breathing, and speed ramps)
- **Veo 3.1** (Google DeepMind video generation model)
- **Runway 4.5**
- **Seedance 2.0**
- **Omni**

### Audio Synthesis
- **ElevenLabs** (optimized using tone markers and pause breaks)
- **Fish Audio** (optimized for conversational room tone replication)
- **Lovo**

---

## License

This project is licensed under the MIT License - see the LICENSE file for details.
# AII-Standard
AII (AI Image Format) is an open, ZIP-based standard for AI-generated images. It packages the image, prompts, seeds, model info, variations, settings, licensing, and provenance into a single .aii file, enabling transparent, reproducible AI-native image workflows.

🖼️ AII – AI Image Format
An open standard for AI-generated images

File extension: .aii
Version: 1.0.0

🎨 Overview

AII (AI Image Format) is an open, ZIP-based container standard for AI-generated images.
It packages the image file, generation prompts, seeds, metadata, model info, variations, licensing, and provenance into a single .aii container.

AII enables transparent attribution, stable reproducibility, and AI-native workflows across editing tools and platforms.

📦 What’s Inside an .aii File?

An .aii file is a ZIP container with this structure:
/
  manifest.json                     # REQUIRED: core metadata for the image
  image/
    main.png                        # REQUIRED: primary image (png/jpg/webp)
    layers/                         # OPTIONAL: separated layer data
    variations/                     # OPTIONAL: alt renders or upscales
  prompts/
    generation.txt                  # OPTIONAL: prompt used
    negative.txt                    # OPTIONAL
    metadata.json                   # OPTIONAL: seed, cfg, steps, etc.
  model/
    model_info.json                 # OPTIONAL: engine/model details
  legal/
    license.txt                     # OPTIONAL: licensing terms
    terms.txt                       # OPTIONAL
  extra/
    notes.md                        # OPTIONAL: custom project notes
The manifest.json defines model details, prompt sources, metadata, and file paths.

🧠 Key Features
✔ Stores AI generation metadata

AII preserves:

Prompt & negative prompt

Seed value

Sampler / guidance settings

Steps, CFG, resolution

AI model name & version

Generator platform (e.g., Midjourney, Stable Diffusion, DALL·E)

Creation timestamp

Essential for reproducibility & authenticity.

✔ One file for everything

A single .aii container includes:

Image

Prompt

Negative prompt

Seed + settings

Model info

Variations/upscales

Layers (optional)

Licensing

Creator identity

Great for archiving, sharing, and verification.

✔ Verifiable provenance

Ensures transparency around:

Who generated the image

With what model

Under what parameters

Perfect for:

AI art platforms

Licensing workflows

Editorial verification

Dataset labeling

✔ Open & extensible

AII uses a ZIP-based architecture, making it easy to:

Add new metadata fields

Support multiple models

Extend layer/variation systems

Plug into pipelines across creative tools

📑 manifest.json Structure (Simplified)
{
  "aii_version": "1.0.0",
  "id": "aii-2025-000001",
  "title": "Sample Image",
  "creator": "CreatorName",
  "resolution": "1024x1024",
  "format": "png",
  "ai_generated": true,

  "ai_source": {
    "tool_name": "Stable Diffusion",
    "tool_version": "v1.6",
    "model_name": "SDXL",
    "prompt_source": "prompts/generation.txt",
    "negative_prompt_source": "prompts/negative.txt",
    "settings_source": "prompts/metadata.json"
  },

  "provenance": {
    "creator_handle": "YourName",
    "creation_utc": "2025-12-05T12:00:00Z",
    "tool_chain": ["SDXL", "AII-WRAPPER v1.0"]
  },

  "files": {
    "main_image": "image/main.png",
    "variations": [
      "image/variations/upscale_1.png"
    ],
    "layers": [],
    "license_file": "legal/license.txt"
  }
}

🧰 Tools (Coming Soon)

Planned utilities:

aiiwrap — wrap image + prompts into .aii

aii-validator — check spec compliance

aiicore — read/write AII containers in code

🌐 MIME Type

Recommended MIME type for .aii:
image/aii

🛠 Use Cases

AI art platforms

Editorial content review

Dataset provenance

Layered AI image workflows

Archiving projects with complete prompt history

Licensing & commercial verification

🔄 Versioning

AII uses semantic versioning:

1.x.x — backward compatible

2.x.x — structural or schema changes

Unknown fields should be ignored for forward compatibility.

📬 Contributing

AII is an open specification, and contributions via issues and pull requests are welcome.

📝 License

Released under the MIT License.

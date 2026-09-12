# Problem Statement

Farmers and agricultural field workers in India frequently need to identify
the breed of a cattle or buffalo but often lack the specialized visual
expertise to do so accurately, particularly for breeds with overlapping
physical traits. Misidentification can lead to poor breeding decisions,
unrealistic milk yield expectations, and difficulty accessing breed-specific
government support schemes.

# Scope of the Project

This project delivers a web-based tool that allows a user to upload a
photograph of a cow or buffalo and receive the top-3 most likely breed
matches, each with a confidence score and supporting breed information
(origin, type, primary use, and physical characteristics). The system
covers 41 common Indian cattle and buffalo breed classes. It is intended
as an accessible identification aid, not a certified pedigree or
veterinary diagnostic tool.

# Target Users

- Farmers and smallholder livestock owners
- Agricultural field workers and extension officers
- Veterinary students
- Anyone needing a quick, non-expert breed reference

# High-Level Features

- Image upload with client-side preview before submission
- Deep-learning-based breed classification (ConvNeXt-Tiny model)
- Top-3 breed predictions with confidence scores
- Detailed breed information (origin, species, type, use, physical features)
- Support for JPG, JPEG, PNG, and WEBP images up to 10 MB
- GPU-accelerated inference with automatic CPU fallback
- Independently deployed, scalable frontend (Vercel) and backend (Render)
# FireRed Image Edit 1.1 Spark AI Hub Image

Thin container wrapper for running a Gradio UI around `FireRedTeam/FireRed-Image-Edit-1.1` on NVIDIA DGX Spark.

Goals:
- no on-device Docker build during Spark AI Hub install
- ARM64 CUDA 13 image suitable for DGX Spark
- model downloads stored in Docker volumes at runtime

This image:
- installs CUDA 13 compatible PyTorch wheels for ARM64
- installs the diffusers-based runtime needed for FireRed Image Edit
- runs a Gradio app for multi-image editing with optional FireRed LoRAs

Interface:
- upload up to 3 input images
- enter an edit prompt
- optionally choose `Covercraft`, `Lightning`, or `Makeup`
- adjust seed, steps, CFG, resolution, and output count

Upstream references:
- Model: https://huggingface.co/FireRedTeam/FireRed-Image-Edit-1.1
- Demo Space: https://huggingface.co/spaces/FireRedTeam/FireRed-Image-Edit-1.1

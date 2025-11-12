# yolo-cat-watch (PyTorch → ONNX → onnx-mlir)

Minimal app that watches a bowl, detects a **cat** in a hardcoded ROI, and sends a WhatsApp message via Twilio when the cat stays ≥ N seconds.

## Quick Start (Dev)
```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt  # (create if you want) else install manually: opencv-python-headless torch onnxruntime twilio pyyaml
python -m app.cli --config configs/sample.yaml

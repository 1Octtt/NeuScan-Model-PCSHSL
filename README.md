# NeuScan-Model-PCSHSL
## 🔽 Download Pre-trained Model & Config

Download the `.zip` file containing the trained PyTorch model and config:

📁 [Download model_files.zip](https://drive.google.com/drive/folders/1PhvkV6lQEvJVd1gQcbR4RdcuQe_d57B5?usp=sharing)

**Files included:**
- `model.pth` – Trained PyTorch model
- `config.json` – Model configuration or label mapping

### 🧭 How to use:

1. Download and extract `model_files.zip`
2. Place files in your project (e.g., `./model_checkpoints/` or as needed)
3. Load them in your code like so:

```python
import torch
import json
from your_model import YourModel  # Replace with actual model class

# Load model
model = YourModel()
model.load_state_dict(torch.load("model_checkpoints/model.pth", map_location="cpu"))
model.eval()

# Load config or labels
with open("model_checkpoints/config.json", "r") as f:
    config = json.load(f)

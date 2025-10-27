Environment:

OS：Ubuntu 22.04

Python：3.11

CUDA 12.x

CUDA Toolkit：Pytorch wheel

GPU: M2 Pro + L40S

Tool & Dependency: 

apt-get update && apt-get install -y git ffmpeg

cd /workspace && rm -rf generative-models && git clone https://github.com/Stability-AI/generative-models.git

cd generative-models && python3 -m venv .gm && source .gm/bin/activate

python -m pip install -U pip wheel

# PyTorch/cu121 + xformers

pip install --index-url https://download.pytorch.org/whl/cu121 \
  "torch==2.1.2" "torchvision==0.16.2"
  
pip install xformers==0.0.23.post1

pip install fire==0.6.0 pytorch-lightning==2.0.9 open-clip-torch==2.24.0 \
  timm==0.9.12 einops==0.7.0 opencv-python-headless==4.8.1.78 \
  numpy==1.26.4 onnxruntime==1.18.1 rembg==2.0.56 imwatermark==0.0.2 \
  decord==0.6.0 transformers==4.41.2 pyyaml==6.0.1
  
#Please pay attention to clip and imwatermark, it is very likely to install a wrong version, if so, please reinstall.

pip install "git+https://github.com/openai/CLIP.git"

pip install imwatermark



🚀generative-modal => official code👑 PS:SV3D series modal expect img input, while SV4D series modal expect mp4 input😱 
you can compare by using entirely static video vs video with an orbit, SV4D likes merry-go-rounds: take away the spin and its noise prediction stops behaving.

🚀input_simple => simple tasks & entire front perspective 2D image🍳

🚀input_difficult => difficult tasks input (explanation available in file name)🥩

🚀output_simple => output of input_simple

🚀output_difficult => output of input_difficult

🚀data => benchmark result

🚀fig => benchmark input

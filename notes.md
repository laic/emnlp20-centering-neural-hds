## Install on stardale

For consistency, let's start with the fastpitch environment: 
https://github.com/dan-wells/eddie-egs/blob/main/B1-eddie-nvidia-apex.sh

This is because the centering code asks for fairseq (though it is not in the dependencies), which suggests apex for speed
https://github.com/facebookresearch/fairseq

```
git clone https://github.com/NVIDIA/apex
cd apex
pip install -v --no-cache-dir --global-option="--cpp_ext" --global-option="--cuda_ext" \
  --global-option="--deprecated_fused_adam" --global-option="--xentropy" \
  --global-option="--fast_multihead_attn" ./
```


---

Issues installing transformers
```
CMake Error at CMakeLists.txt:15 (cmake_minimum_required):
      CMake 3.1 or higher is required.  You are running version 2.8.12.2
```

Update cmake via conda

```
conda install cmake
```

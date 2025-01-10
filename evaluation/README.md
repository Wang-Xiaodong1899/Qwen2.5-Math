### Requirements
You can install the required packages with the following command:
```bash
cd latex2sympy
pip install -e .
cd ..
pip install -r requirements.txt
pip install vllm --upgrade
pip install transformers --upgrade
# pip install vllm==0.5.1 --no-build-isolation
# pip install transformers==4.42.3
```

```
# if encounter rust installation error
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
export PATH="$HOME/.cargo/bin:$PATH"
source ~/.cargo/env
```


### Evaluation
You can evaluate Qwen2.5/Qwen2-Math-Instruct series model with the following command:
```bash
# Qwen2.5-Math-Instruct Series
PROMPT_TYPE="qwen25-math-cot"

CUDA_VISIBLE_DEVICES=0 bash sh/eval.sh "qwen25-math-cot" /workspace/wxd/Llama-3.2-1B-Instruct

```

## Acknowledgement
The codebase is adapted from [math-evaluation-harness](https://github.com/ZubinGou/math-evaluation-harness).

<h1 align="center">🔍 Glance-or-Gaze (GoG)</h1>

<p align="center">
  <em>"You see, but you do not observe. The distinction is clear."</em>
  <br>
  — Arthur Conan Doyle, <em>A Scandal in Bohemia</em>
</p>

<p align="center">
  ─────────────  ✦  ─────────────
</p>

<p align="center">
  <b>The official repository for</b><br>
  <b>"Glance-or-Gaze: Incentivizing LMMs to Adaptively Focus Search via Reinforcement Learning"</b>
</p>

<p align="center">
  📑 <a href="https://arxiv.org/abs/2601.13942"><b>Paper</b></a> &nbsp;•&nbsp;
  🤗 <a href="https://huggingface.co/Edwinzz/GoG-SFT-Qwen2.5-7B">GoG-SFT-Qwen2.5-7B</a> &nbsp;•&nbsp;
  🤗 <a href="https://huggingface.co/Edwinzz/GoG-RL-Qwen2.5-7B">GoG-RL-Qwen2.5-7B</a> &nbsp;•&nbsp;
  🤗 <a href="https://huggingface.co/Edwinzz/GoG-SFT-Qwen3-8B-Thinking">GoG-SFT-Qwen3-8B-Thinking</a> &nbsp;•&nbsp;
  🤗 <a href="https://huggingface.co/Edwinzz/GoG-RL-Qwen3-8B-Thinking">GoG-RL-Qwen3-8B-Thinking</a>
</p>

---

## 📅 Timeline

- **[2026/04/29]** 🚀 We released our model checkpoints, including both SFT and RL versions: [GoG-SFT-Qwen2.5-7B](https://huggingface.co/Edwinzz/GoG-SFT-Qwen2.5-7B), [GoG-RL-Qwen2.5-7B](https://huggingface.co/Edwinzz/GoG-RL-Qwen2.5-7B), [GoG-SFT-Qwen3-8B-Thinking](https://huggingface.co/Edwinzz/GoG-SFT-Qwen3-8B-Thinking), and [GoG-RL-Qwen3-8B-Thinking](https://huggingface.co/Edwinzz/GoG-RL-Qwen3-8B-Thinking)! Evaluation code and dataset will be released soon, stay tuned!

- **[2026/04/06]** 🎉 Our paper *"Glance-or-Gaze: Incentivizing LMMs to Adaptively Focus Search via Reinforcement Learning"* has been accepted to **ACL 2026 Findings**!

## Performance

We compare **Direct Answer**, **Prompt-based GoG**, **Full-Search Workflow**, and **Search-Equipped Models**. 🟦 Blue rows indicate our proposed models (SFT and RL). ⬜ Gray row indicates the reproduced MMSearch-R1 baseline. \* denotes reproduced results.

|  |  | *In-Domain* |  | *Out-of-Domain* |  |  |  |
|:--|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
| **Model** | **Avg.** | **FVQA** | **InfoSeek** | **SimpleVQA** | **MMSearch** | **LiveVQA** | **DynVQA** |
| ***Direct Answer*** | | | | | | | |
| Qwen2.5-VL-7B              | 20.31 | 25.33 | 13.90 | 41.26 | 14.62 | 10.30 | 16.43 |
| Qwen2.5-VL-32B             | 22.79 | 26.89 | 16.95 | 42.84 | 16.37 | 12.70 | 20.96 |
| Qwen3-VL-8B-Instruct       | 21.13 | 23.94 | 13.80 | 40.18 | 15.20 | 11.40 | 22.24 |
| Qwen3-VL-8B-Thinking       | 23.84 | 24.56 | 16.05 | 41.76 | 15.20 | 15.15 | 30.31 |
| Qwen3-VL-30B-A3B-Instruct  | 23.80 | 26.11 | 16.70 | 42.35 | 18.13 | 12.60 | 26.91 |
| Qwen3-VL-30B-A3B-Thinking  | 27.26 | 31.11 | 22.80 | 43.73 | 17.54 | 15.40 | 33.00 |
| GPT-4o                     | 30.68 | 42.00 | 30.60 | 43.44 | 21.64 | 14.80 | 31.59 |
| ***Prompt-based GoG Method*** | | | | | | | |
| Qwen2.5-VL-7B              | 22.31 | 24.50 | 17.40 | 41.66 | 20.47 | 10.40 | 19.41 |
| Qwen3-VL-8B-Think          | 41.70 | 51.33 | 32.00 | 62.69 | 36.84 | 25.95 | 41.36 |
| ***Full-Search Workflow*** | | | | | | | |
| Qwen2.5-VL-7B              | 44.36 | 61.06 | 38.15 | 59.13 | 36.26 | 31.05 | 40.51 |
| Qwen3-VL-8B-Thinking       | 46.99 | 57.33 | 32.25 | 61.90 | 63.84 | 23.55 | 39.09 |
| ***Search-Equipped Models*** | | | | | | | |
| ⬜ MMSearch-R1\*                    | 36.91 | 42.39 | 24.65 | 54.79 | 40.94 | 23.85 | 34.84 |
| 🟦 **GoG-2.5-7B-SFT**              | 43.28 | 53.72 | 41.90 | 60.61 | 40.35 | 24.55 | 38.53 |
| 🟦 **GoG-3-8B-Think-SFT**          | 50.17 | 62.17 | 40.55 | 65.65 | 53.80 | 32.40 | 46.46 |
| 🟦 **GoG-2.5-7B-RL**               | 53.22 | 66.78 | **51.05** | 64.86 | 56.73 | 37.70 | 42.21 |
| 🟦 **GoG-3-8B-Think-RL**           | **56.88** | **68.44** | 49.05 | **66.44** | **65.50** | **43.85** | **48.02** |

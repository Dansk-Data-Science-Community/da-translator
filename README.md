# Motivation
In order to push state-of-the-art for low-resource languages we should consider how we gather data. Plenty of work has gone into sourcing, curating, annotating and preparing data in high-resource languages. 

Can we somehow take advantage of that?

Having an easy to use model that can quickly and accurately translate English to Danish would allow us to capture the value from existing high-quality datasets.

# Vision
Can we train a relatively small (<=4B) model that performs English to Danish translations reasonably well? The size constraint is important for usability. The smaller varients of Gemma3 and Qwen3 both show relatively great performance for on [Danish benchmarks](https://euroeval.com/leaderboards/Monolingual/danish/#__tabbed_1_3), indicating a fair level of general purpose language understanding. The combination of these models along with datasets providing parallel sentences in Danish and English provides the foundation.

# Resources
* Parallel sentences datasets
  * https://huggingface.co/collections/sentence-transformers/parallel-sentences-datasets-6644d644123d31ba5b1c8785
* GemmaX paper
  * https://arxiv.org/abs/2502.02481
* Seed-X-PPO-7B
  * https://huggingface.co/ByteDance-Seed/Seed-X-PPO-7B
* Gemma Fine-tuning guide blog post
  * https://ai.google.dev/gemma/docs/core/huggingface_text_full_finetune
  

# Open Questions / Things to do
* What is current SOTA for Eng->Da translation?
  * Which benchmarks and metrics are commonly used?
    * [Flores](https://huggingface.co/datasets/facebook/flores) 
  * Evaluate GemmaX and Seed-X-PPO-7B
* How is the quality of the parallel sentences? Do we need to do some filtering beforehand?
* Many of these parallel sentences are fairly short. Does translation performance degrade for longer sentences?
* ...

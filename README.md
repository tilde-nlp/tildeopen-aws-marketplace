# TildeOpen 30B 64k on AWS Marketplace: sample notebook and data

Companion repository for the AWS Marketplace listing **TildeOpen 30B 64k (MT / Contextual QA / Summarisation)** by [Tilde](https://tilde.ai).

| Item | Location |
|---|---|
| Sample notebook | [`TildeOpen-30b-64k-MT-CQA-SUM.ipynb`](TildeOpen-30b-64k-MT-CQA-SUM.ipynb) |
| Real-time input samples | [`data/input/real-time/`](data/input/real-time/) |
| Batch input sample | [`data/input/batch/batch_input.jsonl`](data/input/batch/batch_input.jsonl) |
| Real-time output samples | [`data/output/real-time/`](data/output/real-time/) |
| Batch output sample | [`data/output/batch/batch_input.jsonl.out`](data/output/batch/batch_input.jsonl.out) |

## Running the notebook

1. Subscribe to the product in AWS Marketplace.
2. Clone this repository into Amazon SageMaker Studio or a Notebook Instance:
   ```
   git clone https://github.com/tilde-nlp/tildeopen-aws-marketplace.git
   ```
3. Open the notebook with the `conda_python3` kernel and run all cells. The only inputs it needs are the model package ARN table (already filled per Region) and an execution role with SageMaker and S3 access.

## Request format

Requests use the OpenAI chat-completions schema served by vLLM. The `messages` array must follow one of six fixed templates (plain translation, translation with glossary, translation with examples, both, contextual QA, summarisation). See notebook section 2.2 and the input samples.

## Model

- Base model: [TildeAI/TildeOpen-30b-64k](https://huggingface.co/TildeAI/TildeOpen-30b-64k) (CC-BY-4.0)
- Paper: Bergmanis et al., *TildeOpen LLM: Leveraging Curriculum Learning to Achieve Equitable Language Representation*, LREC 2026, https://arxiv.org/abs/2603.08182
- Translation data mix: [TildeAI/TildeOpen-MT-Euro-mix](https://huggingface.co/datasets/TildeAI/TildeOpen-MT-Euro-mix)

## Support

<support email>

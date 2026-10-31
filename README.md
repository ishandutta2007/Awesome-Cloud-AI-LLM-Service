# Awesome-Cloud-AI-LLM-Service

# Awesome-Cloud-AI-LLM-Service
**Top Cloud AI LLM Service (Opensource) 🌟 Star if you like it! 🌟**

**Curated List of SaaS Products & Open-Source GitHub Projects**
*Focused on Model Inference, LLM Gateways, Observability & Self-Hosted Serving Infrastructure*
**Last updated: October 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Cloud AI & LLM Services**. These tools enable organizations to run inference on large language models, route requests across providers, monitor AI applications, and build RAG pipelines—from fully managed cloud AI platforms with proprietary models and enterprise SLAs to open-source inference engines and gateways that give teams complete control over their model serving and AI infrastructure.

**Examples** include OpenAI API, Anthropic API, AWS Bedrock, Google Cloud Vertex AI, Azure OpenAI Service, Snowflake Cortex AI, Databricks Mosaic AI, Mistral AI, Cohere, and Groq Cloud (the category leaders in commercial space).

**Open-source emphasis**: This section is expanded with every relevant project for self-hosted inference, LLM gateways, and open AI infrastructure. **Critical note**: The open-source AI infrastructure landscape is exceptionally mature—**vLLM** dominates inference serving with 73.7K+ stars , **LiteLLM** is the leading multi-provider gateway , and **Langfuse** and **Arize Phoenix** lead observability . However, no open-source project matches OpenAI's model quality or Anthropic's safety research; those are proprietary advantages that open weights cannot replicate at the frontier.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[OpenAI API](https://openai.com/)**
  **Frontier model API** with GPT-4o, o-series reasoning models, and multimodal capabilities. **Pricing**: Per-token pricing varies by model; fine-tuning available. **Free tier**: Limited trial credits. **Best for**: developers wanting the most widely adopted frontier models with broad ecosystem support.

- **[Anthropic API](https://www.anthropic.com/)**
  **Claude model API** with strong reasoning, long context (200K+ tokens), and safety focus. **Pricing**: Per-token pricing; prompt caching reduces costs. **Free tier**: Limited trial. **Best for**: teams prioritizing reasoning quality, long-document analysis, and safety-aligned outputs.

- **[AWS Bedrock](https://aws.amazon.com/bedrock/)**
  **Managed foundation model service** providing access to models from Anthropic, Meta, Mistral, Cohere, and Amazon via a single API. **Pricing**: Per-token or provisioned throughput. **Free tier**: Limited trial. **Best for**: AWS-centric organizations wanting multi-model access without managing infrastructure.

- **[Google Cloud Vertex AI](https://cloud.google.com/vertex-ai)**
  **Enterprise AI platform** with Gemini models, Model Garden (third-party models), and MLOps tooling. **Pricing**: Consumption-based. **Free tier**: Limited credits. **Best for**: Google Cloud organizations wanting integrated model access with enterprise governance.

- **[Azure OpenAI Service](https://azure.microsoft.com/en-us/products/ai-services/openai-service)**
  **Azure-hosted OpenAI models** with enterprise compliance, private networking, and content filtering. **Pricing**: Per-token; provisioned throughput available. **Free tier**: Limited trial. **Best for**: Microsoft-centric enterprises needing OpenAI models with Azure's security and compliance controls.

- **[Snowflake Cortex AI](https://www.snowflake.com/)**
  **AI services within Snowflake** including LLM functions (COMPLETE, SUMMARIZE, TRANSLATE) and Cortex Search for RAG. **Pricing**: Consumption-based on Snowflake credits. **Free tier**: Trial credits. **Best for**: Snowflake customers wanting LLM capabilities without moving data outside the warehouse perimeter.

- **[Databricks Mosaic AI](https://www.databricks.com/)**
  **AI platform** with model serving, fine-tuning, and vector search within the lakehouse. **Pricing**: Consumption-based on Databricks units. **Free tier**: Community Edition limited. **Best for**: Databricks customers wanting to build and serve models on their lakehouse data.

- **[Mistral AI](https://mistral.ai/)**
  **European frontier model API** with Mistral Large, Codestral, and open-weight models. **Pricing**: Per-token pricing. **Free tier**: Limited trial. **Best for**: organizations wanting European data sovereignty and strong multilingual/code capabilities.

- **[Cohere](https://cohere.com/)**
  **Enterprise LLM API** with Command (generation), Embed (embeddings), and Rerank models focused on RAG. **Pricing**: Per-token pricing. **Free tier**: Trial available. **Best for**: enterprises building RAG applications with strong embedding and reranking capabilities.

- **[Groq Cloud](https://groq.com/)**
  **Ultra-low-latency inference API** running open models (Llama, Mixtral, Gemma) on custom LPU hardware. **Pricing**: Per-token; faster than GPU-based providers. **Free tier**: Limited rate-limited access. **Best for**: latency-sensitive applications where response speed is critical.

## Open-Source GitHub Projects

- **[vLLM](https://github.com/vllm-project/vllm)**
  **High-throughput LLM inference engine** (Apache 2.0, **73.7K+ stars**) — **the most widely adopted open-source inference engine** for self-hosted model serving . **Features**: **PagedAttention** for efficient KV cache memory management; **200+ model architectures** supported; multi-GPU support across **NVIDIA, AMD, Intel, and TPU**; OpenAI-compatible API server; continuous batching for high throughput; production-proven at scale. **Tech stack**: Python, CUDA. **Deploy**: Self-hosted (Docker, Kubernetes, cloud VMs). **Trade-off**: **Requires GPU infrastructure**—not a managed service. Operational complexity for multi-node deployments. **Best for**: teams wanting the broadest model support and highest throughput for self-hosted inference—the de facto standard for production LLM serving.

- **[SGLang](https://github.com/sgl-project/sglang)**
  **Fast LLM serving framework** (Apache 2.0, **~20K+ stars**) — **the inference engine with a measurable advantage on RAG and multi-turn workloads** . **Features**: **RadixAttention** for efficient prefix caching across requests; **29% throughput advantage on RAG workloads** compared to alternatives; structured output generation; multi-turn conversation optimization; OpenAI-compatible API. **Tech stack**: Python, CUDA. **Deploy**: Self-hosted. **Trade-off**: **Smaller community than vLLM**; fewer model architectures supported. **Best for**: teams building RAG or multi-turn conversational applications where prefix caching yields significant throughput gains.

- **[LiteLLM](https://github.com/BerriAI/litellm)**
  **Open-source LLM gateway and proxy** (MIT, **18K+ stars**) — **the most widely adopted multi-provider gateway** for unifying access to 100+ LLM APIs . **Features**: **OpenAI-compatible proxy**—call any provider using the OpenAI format; **100+ providers supported** (OpenAI, Anthropic, Azure, Bedrock, Vertex, Cohere, Mistral, local models); **virtual keys** with budget and rate limits; **cost tracking** and spend management; **guardrails** and fallback chains; **MCP support**; load balancing across deployments. **Tech stack**: Python (with Rust core for performance). **Deploy**: Self-hosted (`pip install litellm[proxy]`) or LiteLLM Cloud. **Trade-off**: **No semantic caching** in the open-source version; some advanced enterprise features require the commercial offering . **Best for**: teams wanting a single OpenAI-compatible endpoint across multiple providers with cost tracking and virtual keys—the pragmatic default for multi-model applications.

- **[TensorRT-LLM](https://github.com/NVIDIA/TensorRT-LLM)**
  **NVIDIA-optimized inference engine** (Apache 2.0 + closed components) — **the highest-throughput option on NVIDIA hardware**, delivering **30–60% faster performance than vLLM on H100** GPUs . **Features**: NVIDIA TensorRT compilation for maximum GPU utilization; optimized kernels for NVIDIA architectures; in-flight batching; multi-GPU and multi-node support. **Tech stack**: C++/Python, CUDA. **Deploy**: Self-hosted (NVIDIA GPUs required). **Trade-off**: **NVIDIA lock-in**—does not run on AMD or Intel GPUs. **Closed-source components** reduce auditability. More complex setup than vLLM. **Best for**: teams with NVIDIA GPU fleets prioritizing maximum throughput over portability—especially when H100/H200 utilization directly impacts cost.

- **[Ollama](https://github.com/ollama/ollama)**
  **Local LLM runtime with one-command model management** (MIT, **100K+ stars** via llama.cpp ecosystem) — **the simplest way to run models locally** . **Features**: One-command model pull and run (`ollama run llama3`); OpenAI-compatible API; model library with popular open-weight models (Llama, Mistral, Gemma, Phi); runs on macOS, Linux, and Windows; Apple Silicon optimized; **52M monthly downloads** . **Tech stack**: Go, llama.cpp. **Deploy**: Local desktop or server (`ollama serve`). **Trade-off**: **Not for multi-tenant production**—designed for local development and single-user scenarios . Limited concurrency and throughput compared to vLLM. **Best for**: developers wanting to run models locally for prototyping, privacy-sensitive single-user workloads, or edge deployments—not production multi-tenant serving.

- **[llama.cpp](https://github.com/ggerganov/llama.cpp)**
  **Efficient LLM inference in C/C++** (MIT, **100K+ stars**) — **the most portable inference engine**, running on everything from Raspberry Pi to high-end GPUs . **Features**: **GGUF model format**; Metal, CUDA, Vulkan, and ROCm backends; ARM and x86 support; quantization (2-bit to 8-bit); CPU inference without GPU; runs on macOS, Linux, Windows, and mobile. **Tech stack**: C/C++. **Deploy**: CLI, server mode, or embedded in applications. **Trade-off**: **Lower throughput than GPU-optimized engines** for large-scale serving. Best for edge and local use. **Best for**: teams needing to run models on constrained hardware—laptops, Raspberry Pi, mobile devices, or CPU-only servers where GPU inference is impractical.

- **[Langfuse](https://github.com/langfuse/langfuse)**
  **Open-source LLM observability and evaluation platform** (MIT, **35K+ stars**) — **the most starred open-source observability platform for LLM applications** . **Features**: **Tracing** for LLM calls, agent workflows, and RAG pipelines; **evaluation** with LLM-as-judge and custom evaluators; **prompt management** with versioning; **datasets** for testing; **cost and latency tracking**; self-hosted or cloud. **Tech stack**: TypeScript, Python, PostgreSQL. **Deploy**: Self-hosted (Docker) or Langfuse Cloud. **Trade-off**: **Observability only**—not an inference engine or gateway. **Best for**: teams running LLM applications in production needing traces, evaluations, and cost visibility—the open-source alternative to LangSmith.

- **[Arize Phoenix](https://github.com/Arize-ai/phoenix)**
  **Open-source AI observability and evaluation** (Apache 2.0, **11.8K+ stars**) — **a focused alternative to Langfuse** with strong evaluation capabilities . **Features**: LLM tracing and spans; **evaluation** with built-in and custom metrics; **RAG analysis** for retrieval quality; datasets and experiments; OpenTelemetry-native. **Tech stack**: Python, TypeScript. **Deploy**: Self-hosted (Docker, pip) or Arize Cloud. **Trade-off**: **Smaller community than Langfuse**; fewer prompt management features. **Best for**: teams wanting OpenTelemetry-native LLM observability with strong RAG evaluation—especially those already using OpenTelemetry elsewhere.

- **[Qdrant](https://github.com/qdrant/qdrant)**
  **Vector database for RAG and semantic search** (Apache 2.0, **~20K+ stars**) — **the pragmatic default for production RAG** . **Features**: **Rust-based** for performance; **filterable HNSW** indexing; payload filtering with tenant isolation; hybrid search (vector + keyword); quantization for memory efficiency; multi-tenancy support; replication and RBAC in open-source build . **Tech stack**: Rust. **Deploy**: Self-hosted (Docker, Kubernetes) or Qdrant Cloud. **Trade-off**: **No native encryption at rest**—relies on infrastructure disk encryption . **Best for**: teams building RAG applications needing production-grade vector search with filtering, multi-tenancy, and strong performance—the most balanced open-source vector database for LLM applications.

### Additional Strong Open-Source Options

- **Bifrost** — Apache 2.0 LLM gateway with 11µs P99 latency and semantic caching . **Note**: 20+ providers; Go-based; MCP support. **Best for**: teams hitting Python gateway performance ceilings or needing semantic caching at the gateway layer .
- **Portkey Gateway** — Apache 2.0 core gateway with routing across 250+ providers . **Note**: Guardrails and semantic caching require the managed cloud tier. **Best for**: teams wanting guardrails and semantic caching out of the box, comfortable with open-core split .
- **RouteLLM** — Apache 2.0 routing framework from LMSYS . **Note**: **Router, not a gateway**—decides which model should handle a request; achieves ~95% of GPT-4 quality at 14% of call volume on benchmarks . **Best for**: teams with a gateway already deployed wanting to add cost-optimizing routing on top.
- **OpenLIT** — OpenTelemetry-native LLM observability with GPU monitoring . **Note**: Broader than pure LLM tracing—includes GPU metrics and guardrails. **Best for**: teams wanting unified LLM and GPU observability.

**Frameworks for building custom systems**: Combine **vLLM** or **SGLang** for inference serving with **LiteLLM** as the gateway, **Qdrant** for vector search, and **Langfuse** for observability—creating a complete self-hosted LLM stack. **None of these match OpenAI's frontier model quality or Anthropic's safety research**; those remain proprietary advantages. The open-source stack is for teams that prioritize control, cost, and data sovereignty over access to the absolute frontier.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, license (for open-source), and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Cloud AI and LLM services handling prompts and model outputs must comply with data protection regulations (GDPR, CCPA, etc.) and implement appropriate access controls, content filtering, and audit logging.
- **The "frontier model API" vs. "inference engine" vs. "LLM gateway" vs. "observability platform" distinction is critical.** **OpenAI, Anthropic, Mistral, Cohere, and Groq** provide **proprietary model access**—their value is the model itself, not the infrastructure . **AWS Bedrock, Vertex AI, Azure OpenAI, Snowflake Cortex, and Databricks Mosaic** are **managed platforms**—they provide model access with cloud integration but lock you into their ecosystem. **vLLM, SGLang, TensorRT-LLM, llama.cpp, and Ollama** are **inference engines**—they serve open-weight models you host yourself . **LiteLLM, Bifrost, Portkey, and RouteLLM** are **gateways/routers**—they unify access to multiple providers but do not serve models . **Langfuse and Arize Phoenix** are **observability platforms**—they monitor AI applications but do not serve or route models . **Qdrant** is a **vector database**—it stores embeddings for RAG, not models. **Choose based on whether you need model access, serving, routing, or monitoring.**
- **vLLM is the default choice for self-hosted inference.** 73.7K+ stars, 200+ model architectures, multi-GPU support across vendors, and production-proven at scale . **SGLang is the better choice specifically for RAG and multi-turn workloads**, with a 29% throughput advantage on those patterns . **TensorRT-LLM is the throughput leader on NVIDIA H100** (30–60% faster than vLLM) but locks you to NVIDIA hardware .
- **LiteLLM is the pragmatic default for multi-provider gateways.** 100+ providers, OpenAI-compatible proxy, virtual keys with budget controls, and cost tracking—all under MIT license . **The trade-off**: no semantic caching in the open-source version; some features require the commercial offering . **Bifrost is the alternative for performance-sensitive teams** (11µs P99) with semantic caching included .
- **Ollama is for local development, not production serving.** 52M monthly downloads and one-command simplicity make it excellent for prototyping, but it is **explicitly not for multi-tenant production** . **llama.cpp is for edge deployments**—it runs on Raspberry Pi, mobile, and CPU-only servers where GPU inference is impractical .
- **Pricing opacity is universal across commercial AI providers.** OpenAI, Anthropic, AWS Bedrock, Vertex AI, Azure OpenAI, Snowflake Cortex, Databricks Mosaic, Mistral, Cohere, and Groq all publish per-token pricing, but volume discounts and enterprise terms require sales contact. **Validate with direct vendor conversations against your token volume and latency requirements.**
- Self-hosted open-source solutions require significant infrastructure (GPU servers for inference engines, vector database storage for Qdrant, monitoring backends for observability), security hardening for model endpoints, and ongoing maintenance. **LLM inference is GPU-intensive**—ensure your infrastructure planning accounts for GPU availability, cooling, and power costs before committing to self-hosting.

---

**Made for AI engineers, platform teams, and organizations building transparent cloud AI and LLM infrastructure.**
Let's make Cloud AI & LLM Services more open, data-driven, and cost-effective.

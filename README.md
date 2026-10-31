# Awesome-Cloud-AI-LLM-Service

**Top Cloud AI LLM Service (Opensource) 🌟 Star if you like it! 🌟**

**Curated List of SaaS Products & Open-Source GitHub Projects**

*Focused on Model Inference, LLM Gateways, Observability & Self-Hosted Serving Infrastructure*

**Last updated: October 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Cloud AI & LLM Services**. These tools enable organizations to run inference on large language models, route requests across providers, monitor AI applications, and build RAG pipelines—from fully managed cloud AI platforms with proprietary models and enterprise SLAs to open-source inference engines and gateways that give teams complete control over their model serving and AI infrastructure.

**Examples** include OpenAI API, Anthropic API, AWS Bedrock, Google Cloud Vertex AI, Azure OpenAI Service, Snowflake Cortex AI, Databricks Mosaic AI, Mistral AI, Cohere, and Groq Cloud (the category leaders in commercial space).

**Open-source emphasis**: This section is expanded with every relevant project for self-hosted inference, LLM gateways, and open AI infrastructure. **Critical note**: The open-source AI infrastructure landscape is exceptionally mature—**vLLM** dominates inference serving with 95K+ stars, **LiteLLM** is the leading multi-provider gateway, and **Langfuse** and **Arize Phoenix** lead observability. However, no open-source project matches OpenAI's model quality or Anthropic's safety research; those are proprietary advantages that open weights cannot replicate at the frontier.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents

- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [SaaS/Hosted Platforms](#saashosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

---

## Sector Overview & Market Dynamics

The global Cloud AI & Enterprise LLM Services market is valued at approximately **$88B–$116B in 2025** and is projected to expand beyond **$114B–$230B+ in 2026**, registering a rapid CAGR exceeding 25–35%.

Market concentration exhibits a **dual dynamic**: the upstream foundation model and hyperscale compute layer is **highly concentrated (oligopolistic)** among hyperscalers (Microsoft, Alphabet, Amazon) and leading frontier AI labs (OpenAI, Anthropic), while the downstream application, orchestration, specialized tooling, and gateway layer is **moderately fragmented** with intense competition across niche SaaS providers and an exceptionally mature open-source ecosystem.

---

## SaaS/Hosted Platforms

| Platform | Valuation / Company Size | Pricing | Free Tier / Trial Limits | Description & Best For |
| :--- | :--- | :--- | :--- | :--- |
| **[Azure OpenAI Service](https://azure.microsoft.com/en-us/products/ai-services/openai-service)** | **$3.88T Market Cap** (Microsoft) | Starting at **$0.15 / 1M input tokens** & **$0.60 / 1M output tokens** (GPT-4o-mini); provisioned throughput available | **$200 free credit valid for 30 days** across Azure services upon initial signup | Azure-hosted OpenAI models with enterprise compliance, private networking, and content filtering. Best for Microsoft-centric enterprises needing strict compliance. |
| **[Google Cloud Vertex AI](https://cloud.google.com/vertex-ai)** | **$3.46T Market Cap** (Alphabet) | Starting at **$0.10 / 1M input tokens** & **$0.40 / 1M output tokens** (Gemini Flash); Pro models start at $2.00 / 1M input tokens | **$300 free trial credits valid for 90 days** for new Google Cloud accounts | Enterprise AI platform with Gemini models, Model Garden, and MLOps tooling. Best for Google Cloud organizations needing enterprise governance. |
| **[AWS Bedrock](https://aws.amazon.com/bedrock/)** | **$2.60T Market Cap** (Amazon) | Starting at **$0.06 / 1M input tokens** & **$0.24 / 1M output tokens** (Amazon Nova Micro); Anthropic Claude models priced per-token with prompt caching | **Up to $200 in AWS promotional credits** for new accounts (no permanent free tier; billed from first request) | Managed foundation model service providing access to Anthropic, Meta, Mistral, Cohere, and Amazon models via unified API. Best for AWS-centric teams. |
| **[OpenAI API](https://openai.com/)** | **$852B Valuation** (OpenAI) | Starting at **$0.15 / 1M input tokens** & **$0.60 / 1M output tokens** (GPT-4o-mini); minimum prepaid purchase is $5 | **$100/mo spend limit ceiling on Free Tier** (calls require paid credit or ChatGPT Pro/Business $100–$500/mo bundled credit grant) | Frontier model API with GPT-4o, o-series reasoning models, and multimodal capabilities. Best for developers wanting industry-standard frontier models. |
| **[Anthropic API](https://www.anthropic.com/)** | **$965B Valuation / Pre-IPO** (Anthropic) | Starting at **$0.25 / 1M input tokens** & **$1.25 / 1M output tokens** (Claude 3.5 Haiku); prompt caching discounts up to 90% | **$5 one-time initial credit trial** upon phone verification (or $100–$200/mo credit for Claude Max/Ultra subscribers) | Claude model API with strong reasoning, long context (200K+ tokens), and safety alignment. Best for complex reasoning and long-document analysis. |
| **[Databricks Mosaic AI](https://www.databricks.com/)** | **$190B Valuation** (Databricks) | Starting at **$0.07 per DBU** for serverless model serving endpoints; foundation model queries billed per DBU or per-token | **14-day full-platform free trial** (Community Edition has limited compute; cloud infrastructure billed separately) | Model serving, fine-tuning, and vector search tightly integrated inside the Lakehouse architecture. Best for Databricks Lakehouse customers. |
| **[Snowflake Cortex AI](https://www.snowflake.com/)** | **$115B Market Cap** (Snowflake) | Starting at **$2.00 per AI Credit** for global routing plus underlying virtual warehouse credit consumption | **$400 in free trial credits valid for 30 days** upon creating a new Snowflake trial account | Managed AI functions (COMPLETE, SUMMARIZE, TRANSLATE) and Cortex Search inside Snowflake perimeter. Best for SQL/data warehouse workflows. |
| **[Mistral AI](https://mistral.ai/)** | **$24B Valuation** (Mistral AI) | Starting at **$0.15 / 1M input tokens** & **$0.60 / 1M output tokens** (Ministral 3B); Mistral Large starts at $0.50 / 1M input tokens | **Free Tier forever mode on La Plateforme**: rate-limited to ~1 request/sec (30 RPM) for model experimentation | European frontier model API offering open-weight and proprietary models. Best for European data sovereignty and efficient open weights. |
| **[Cohere](https://cohere.com/)** | **$20B Valuation** (Cohere) | Starting at **$0.15 / 1M input tokens** & **$0.60 / 1M output tokens** (Command R); Embed at $0.10 / 1M tokens, Rerank at $2.00 / 1K searches | **Free Trial Key**: 1,000 API calls per month forever (strictly non-commercial/evaluation use, capped at 20 RPM chat) | Enterprise LLM API with Command, Embed, and Rerank models optimized for enterprise RAG workflows. Best for search, retrieval, and reranking. |
| **[Groq Cloud](https://groq.com/)** | **$3.5B Valuation** (Groq) | Starting at **$0.05 / 1M input tokens** & **$0.08 / 1M output tokens** (Llama 3.1 8B on custom LPUs); on-demand token billing | **Free Tier forever**: 30 requests per minute (RPM) and 6,000 to 30,000 tokens per minute (TPM) limit per organization | Ultra-low-latency inference API serving open-weight models on proprietary LPU hardware. Best for real-time and voice-agent latency-critical apps. |

---

## Open-Source GitHub Projects

Sorted by GitHub Stargazers (descending):

- **[Ollama](https://github.com/ollama/ollama)** [![Stars](https://img.shields.io/github/stars/ollama/ollama?style=social&color=white)](https://github.com/ollama/ollama/stargazers)  
  **Local LLM runtime with one-command model management** (MIT) — **the simplest way to run models locally**.  
  *Features*: One-command model pull and run (`ollama run llama3`), OpenAI-compatible REST API, model library covering Llama, Mistral, Gemma, and Phi, and Apple Silicon / GPU optimization.  
  *Trade-off*: Not designed for multi-tenant high-concurrency production serving.  
  *Best for*: Local development, prototyping, edge applications, and privacy-sensitive single-user deployments.

- **[Dify](https://github.com/langgenius/dify)** [![Stars](https://img.shields.io/github/stars/langgenius/dify?style=social&color=white)](https://github.com/langgenius/dify/stargazers)  
  **Production-ready LLM application development platform** (Apache 2.0) — **leading open-source LLMOps and agent platform**.  
  *Features*: Visual prompt engineering, RAG pipeline orchestration, multi-agent workflows, model management across 50+ providers, and built-in analytics.  
  *Trade-off*: Full self-hosted setup requires multiple supporting services (PostgreSQL, Redis, Celery, Vector DB).  
  *Best for*: Teams building full-stack conversational AI, agent workflows, and enterprise RAG without rebuilding middleware.

- **[Open WebUI](https://github.com/open-webui/open-webui)** [![Stars](https://img.shields.io/github/stars/open-webui/open-webui?style=social&color=white)](https://github.com/open-webui/open-webui/stargazers)  
  **Self-hosted AI interface for Ollama, vLLM, and OpenAI-compatible APIs** (MIT) — **the premier user interface for self-hosted AI**.  
  *Features*: Granular role-based access control (RBAC), built-in RAG with document upload, web search integration, voice/multimodal support, and multi-model chat.  
  *Trade-off*: UI and gateway frontend; depends on underlying inference engines to serve models.  
  *Best for*: Organizations delivering a secure, private, enterprise-grade ChatGPT alternative to internal teams.

- **[llama.cpp](https://github.com/ggerganov/llama.cpp)** [![Stars](https://img.shields.io/github/stars/ggerganov/llama.cpp?style=social&color=white)](https://github.com/ggerganov/llama.cpp/stargazers)  
  **Efficient LLM inference in pure C/C++** (MIT) — **the most portable inference engine in the AI ecosystem**.  
  *Features*: Creator of the GGUF model format, support for 1.5-bit to 8-bit integer quantization, Metal/CUDA/Vulkan/ROCm backends, and CPU-only execution without discrete GPU.  
  *Trade-off*: Lower raw multi-user concurrency and batched throughput compared to dedicated distributed engines like vLLM.  
  *Best for*: Edge devices, laptops, consumer hardware, and resource-constrained environments where running GPU fleets is impractical.

- **[vLLM](https://github.com/vllm-project/vllm)** [![Stars](https://img.shields.io/github/stars/vllm-project/vllm?style=social&color=white)](https://github.com/vllm-project/vllm/stargazers)  
  **High-throughput and memory-efficient LLM inference and serving engine** (Apache 2.0) — **the de facto production standard for self-hosted LLM serving**.  
  *Features*: PagedAttention for near-zero memory waste in KV cache, continuous batching, chunked prefill, tensor parallelism across NVIDIA/AMD/Intel GPUs and TPUs, and full OpenAI-compatible API.  
  *Trade-off*: Requires dedicated GPU infrastructure and operational expertise for multi-node cluster configurations.  
  *Best for*: Production multi-tenant model serving needing maximum throughput, broad architecture compatibility, and battle-tested stability.

- **[LiteLLM](https://github.com/BerriAI/litellm)** [![Stars](https://img.shields.io/github/stars/BerriAI/litellm?style=social&color=white)](https://github.com/BerriAI/litellm/stargazers)  
  **Universal LLM proxy and gateway** (MIT) — **the industry standard multi-provider router**.  
  *Features*: Unified OpenAI-compatible format for 100+ LLM providers, virtual team keys with budget caps and rate limits, spend tracking, failover load balancing, and guardrail hooks.  
  *Trade-off*: Open-source version lacks advanced semantic caching; enterprise governance features require commercial license.  
  *Best for*: Teams calling multiple foundation model providers who need a single proxy with cost controls and key management.

- **[Milvus](https://github.com/milvus-io/milvus)** [![Stars](https://img.shields.io/github/stars/milvus-io/milvus?style=social&color=white)](https://github.com/milvus-io/milvus/stargazers)  
  **Distributed open-source vector database built for massive-scale AI similarity search** (Apache 2.0).  
  *Features*: Cloud-native decoupled architecture, billion-scale vector indexing, hardware acceleration (GPU indexing), hybrid search, and multi-tenancy.  
  *Trade-off*: Distributed architecture introduces operational complexity for small deployments.  
  *Best for*: Massive enterprise RAG deployments searching hundreds of millions to billions of vector embeddings.

- **[SGLang](https://github.com/sgl-project/sglang)** [![Stars](https://img.shields.io/github/stars/sgl-project/sglang?style=social&color=white)](https://github.com/sgl-project/sglang/stargazers)  
  **Fast serving framework for large language and reasoning models** (Apache 2.0) — **the prefix-caching throughput leader**.  
  *Features*: RadixAttention for automatic KV cache reuse across multi-turn chats and shared prompts, 29%+ throughput speedup on RAG workloads, and high-performance structured JSON decoding.  
  *Trade-off*: Smaller hardware support matrix and ecosystem compared to vLLM.  
  *Best for*: RAG applications, multi-agent frameworks, and structured output extraction workloads benefiting heavily from prefix caching.

- **[Langfuse](https://github.com/langfuse/langfuse)** [![Stars](https://img.shields.io/github/stars/langfuse/langfuse?style=social&color=white)](https://github.com/langfuse/langfuse/stargazers)  
  **Open-source LLM engineering platform for observability and evaluation** (MIT) — **the leading open-source observability suite**.  
  *Features*: Detailed request tracing across nested chains and agents, prompt management with version control, LLM-as-a-judge automated evaluations, and granular cost/latency analytics.  
  *Trade-off*: Observability and telemetry only; does not serve models or proxy requests directly.  
  *Best for*: Engineering teams requiring production observability, evaluation pipelines, and regression testing for LLM apps.

- **[Qdrant](https://github.com/qdrant/qdrant)** [![Stars](https://img.shields.io/github/stars/qdrant/qdrant?style=social&color=white)](https://github.com/qdrant/qdrant/stargazers)  
  **High-performance vector database and search engine** (Apache 2.0) — **the pragmatic default for production RAG**.  
  *Features*: Written in Rust, payload-based filtering with HNSW indexing, memory-efficient quantization (scalar and product), and tenant isolation.  
  *Trade-off*: Requires separate disk encryption management at the infrastructure level.  
  *Best for*: Production RAG systems requiring fast semantic search with complex metadata filtering.

- **[Chroma](https://github.com/chroma-core/chroma)** [![Stars](https://img.shields.io/github/stars/chroma-core/chroma?style=social&color=white)](https://github.com/chroma-core/chroma/stargazers)  
  **AI-native open-source embedding database** (Apache 2.0) — **developer-first lightweight vector store**.  
  *Features*: Seamless Python/JavaScript integration, in-memory or server deployment modes, built-in embedding generation, and rapid setup.  
  *Trade-off*: Primarily optimized for small-to-medium datasets; less tailored for multi-billion vector distributed scale.  
  *Best for*: Rapid prototyping, testing, and small-to-medium scale RAG applications.

- **[Weaviate](https://github.com/weaviate/weaviate)** [![Stars](https://img.shields.io/github/stars/weaviate/weaviate?style=social&color=white)](https://github.com/weaviate/weaviate/stargazers)  
  **Open-source cloud-native vector search engine with hybrid search and generative modules** (BSD-3-Clause).  
  *Features*: Native BM25 + vector hybrid search, built-in vectorization modules, multi-modal vector search, and GraphQL API interface.  
  *Trade-off*: Memory consumption can be high for large unquantized indexes.  
  *Best for*: Applications needing out-of-the-box hybrid keyword-vector search and integrated vectorization pipelines.

- **[TensorRT-LLM](https://github.com/NVIDIA/TensorRT-LLM)** [![Stars](https://img.shields.io/github/stars/NVIDIA/TensorRT-LLM?style=social&color=white)](https://github.com/NVIDIA/TensorRT-LLM/stargazers)  
  **NVIDIA-optimized inference library for high-performance LLM serving** (Apache 2.0).  
  *Features*: Deep TensorRT compilation, custom FP8 kernels for Hopper/Blackwell GPUs, in-flight batching, and maximum hardware FLOPs utilization.  
  *Trade-off*: Strict NVIDIA hardware dependency; closed-source driver components and steep setup curve.  
  *Best for*: Enterprise infrastructure teams running high-volume NVIDIA GPU fleets where hardware efficiency and latency are the primary drivers.

- **[Portkey Gateway](https://github.com/portkey-ai/gateway)** [![Stars](https://img.shields.io/github/stars/portkey-ai/gateway?style=social&color=white)](https://github.com/portkey-ai/gateway/stargazers)  
  **Ultra-fast AI gateway connecting to 250+ LLMs with unified API** (Apache 2.0).  
  *Features*: Lightweight footprint (<10MB), sub-millisecond overhead, automatic fallbacks, load balancing, retries, and multi-provider routing.  
  *Trade-off*: Advanced semantic caching and complex enterprise guardrails split into managed cloud offering.  
  *Best for*: Production apps needing a lean, performant API router with automatic retries and multi-provider fallback.

- **[OpenLLM](https://github.com/bentoml/OpenLLM)** [![Stars](https://img.shields.io/github/stars/bentoml/OpenLLM?style=social&color=white)](https://github.com/bentoml/OpenLLM/stargazers)  
  **Fine-tune, serve, and deploy any open-source LLM into production** (Apache 2.0).  
  *Features*: Powered by BentoML and vLLM runtime, one-command model serving, Bento packaging for Kubernetes/BentoCloud, and OpenAI-compatible endpoints.  
  *Trade-off*: Additional packaging layer compared to running bare vLLM directly.  
  *Best for*: Teams standardizing their LLM serving and model fine-tuning within the BentoML production deployment ecosystem.

- **[Arize Phoenix](https://github.com/Arize-ai/phoenix)** [![Stars](https://img.shields.io/github/stars/Arize-ai/phoenix?style=social&color=white)](https://github.com/Arize-ai/phoenix/stargazers)  
  **AI observability, evaluation, and tracing platform** (Apache 2.0) — **OpenTelemetry-native AI monitoring**.  
  *Features*: Native OpenTelemetry tracing, RAG retrieval benchmarking, evaluation metrics with LLM-as-a-judge, and seamless notebook evaluation workflows.  
  *Trade-off*: Smaller prompt-management ecosystem compared to Langfuse.  
  *Best for*: Organizations already invested in OpenTelemetry standards looking for deep RAG evaluation and trace visualization.

- **[Triton Inference Server](https://github.com/triton-inference-server/server)** [![Stars](https://img.shields.io/github/stars/triton-inference-server/server?style=social&color=white)](https://github.com/triton-inference-server/server/stargazers)  
  **NVIDIA multi-framework enterprise inference serving platform** (BSD-3-Clause).  
  *Features*: Multi-framework support (TensorRT-LLM, PyTorch, ONNX, TensorFlow), concurrent model execution on shared GPUs, dynamic batching, and enterprise gRPC/HTTP endpoints.  
  *Trade-off*: Higher architectural complexity and configuration overhead than LLM-specific single-binary engines.  
  *Best for*: Large enterprise production platforms serving heterogeneous machine learning models alongside LLMs.

- **[Text Generation Inference (TGI)](https://github.com/huggingface/text-generation-inference)** [![Stars](https://img.shields.io/github/stars/huggingface/text-generation-inference?style=social&color=white)](https://github.com/huggingface/text-generation-inference/stargazers)  
  **Hugging Face production LLM serving engine** (Open-source / OpenRAIL).  
  *Features*: Tensor parallelism, continuous batching, token streaming via SSE, optimized flash-attention, and tight integration with the Hugging Face Hub.  
  *Trade-off*: Transitioned some components to customized open-core licensing; less flexible multi-vendor accelerator matrix than vLLM.  
  *Best for*: Organizations with architectures deeply integrated into Hugging Face Hub models and Hugging Face Enterprise.

- **[Xinference](https://github.com/xorbitsai/inference)** [![Stars](https://img.shields.io/github/stars/xorbitsai/inference?style=social&color=white)](https://github.com/xorbitsai/inference/stargazers)  
  **Distributed inference framework for LLMs, image, and multimodal models** (Apache 2.0).  
  *Features*: Unifies LLM serving, embedding models, speech-to-text, and image generation under one cluster manager with built-in model caching and load distribution.  
  *Trade-off*: Newer ecosystem compared to standalone engines.  
  *Best for*: Teams requiring a single self-hosted cluster to run LLMs, diffusion models, and embeddings concurrently.

- **[BentoML](https://github.com/bentoml/BentoML)** [![Stars](https://img.shields.io/github/stars/bentoml/BentoML?style=social&color=white)](https://github.com/bentoml/BentoML/stargazers)  
  **Unified model serving framework for software engineering and AI applications** (Apache 2.0).  
  *Features*: Multi-model pipelines, adaptive batching, containerization automation, and cloud-native deployment across any infrastructure.  
  *Trade-off*: General ML serving framework; requires pairing with OpenLLM or vLLM for optimized LLM token generation.  
  *Best for*: Engineering teams building composite AI services combining LLMs with traditional ML algorithms.

- **[RouteLLM](https://github.com/lm-sys/RouteLLM)** [![Stars](https://img.shields.io/github/stars/lm-sys/RouteLLM?style=social&color=white)](https://github.com/lm-sys/RouteLLM/stargazers)  
  **Intelligent routing framework for LLMs from LMSYS** (Apache 2.0) — **cost-optimizing smart router**.  
  *Features*: Dynamic routing trained on LMSYS Chatbot Arena data to route simple queries to cheap models and complex queries to frontier models, maintaining ~95% frontier quality at ~14% cost.  
  *Trade-off*: Pure algorithmic router; requires an underlying gateway or proxy (e.g., LiteLLM) to perform actual dispatch.  
  *Best for*: Production systems seeking dramatic cost reductions through automated query-complexity routing.

- **[OpenLIT](https://github.com/openlit/openlit)** [![Stars](https://img.shields.io/github/stars/openlit/openlit?style=social&color=white)](https://github.com/openlit/openlit/stargazers)  
  **OpenTelemetry-native AI and GPU observability tool** (Apache 2.0).  
  *Features*: Auto-instrumentation for 30+ LLM providers and vector DBs, integrated NVIDIA GPU utilization and temperature monitoring, and export to Prometheus/Grafana.  
  *Trade-off*: Emerging project with smaller community than Langfuse.  
  *Best for*: Infrastructure engineers wanting unified tracing for both LLM calls and physical GPU performance.

---

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, license (for open-source), and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

---

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Cloud AI and LLM services handling prompts and model outputs must comply with data protection regulations (GDPR, CCPA, etc.) and implement appropriate access controls, content filtering, and audit logging.
- **The "frontier model API" vs. "inference engine" vs. "LLM gateway" vs. "observability platform" distinction is critical.**
  - **OpenAI, Anthropic, Mistral, Cohere, and Groq** provide **proprietary model access**—their value is the model itself and managed endpoints.
  - **AWS Bedrock, Vertex AI, Azure OpenAI, Snowflake Cortex, and Databricks Mosaic** are **managed enterprise platforms**—they provide model access with deep cloud integration.
  - **vLLM, SGLang, TensorRT-LLM, llama.cpp, TGI, and Ollama** are **inference engines**—they serve open-weight models you host yourself.
  - **LiteLLM, Portkey Gateway, and RouteLLM** are **gateways/routers**—they unify access to multiple providers, balance traffic, and optimize costs.
  - **Langfuse, Arize Phoenix, and OpenLIT** are **observability platforms**—they monitor, evaluate, and trace AI applications.
  - **Milvus, Qdrant, Chroma, and Weaviate** are **vector databases**—they store embeddings for RAG workflows.
- Self-hosted open-source solutions require significant infrastructure (GPU servers for inference engines, vector database storage for RAG, monitoring backends for observability). LLM inference is GPU-intensive—ensure infrastructure planning accounts for GPU availability, cooling, and power costs before committing to self-hosting.

---

**Made for AI engineers, platform teams, and organizations building transparent cloud AI and LLM infrastructure.**

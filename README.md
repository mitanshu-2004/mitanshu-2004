# Mitanshu Goel

Final-year ECE at MAIT Delhi, graduating June 2026. Currently writing a real-time C++17 control loop for a bimanual VR teleoperation rig at Variety Innovation / Enferent.ai — Meta Quest 3 driving two Elite Robots CS66 industrial arms, with `SCHED_FIFO` scheduling and `mlockall` to keep the loop deterministic.

Two strands of work I keep coming back to: real-time robotics on industrial hardware, and continued-pretraining of small foundation models on data I scraped myself.

On the robotics side: an 18-DoF [Hexapod](https://github.com/atom-robotics-lab/Hexapod) at the lab I'm in (atom-robotics-lab @ MAIT) — I own the URDF, the 305-line `ros2_control` hardware interface, and the Gazebo Classic → Ignition Fortress migration. The analytic IK is my collaborator Akshat's work. Now extending the same skill set into bimanual teleop on industrial arms at Enferent.

On the foundation-models side: five training runs across Mistral 7B (LoRA r=128 and r=256), Qwen 2.5 (3B at r=16 and 7B at r=128), and a from-scratch nanoGPT, all on a self-scraped Reddit corpus. Adapters and configs are on [huggingface.co/mitanshugoel](https://huggingface.co/mitanshugoel). The choices that show up across the scripts — embedding LR 5–10× smaller than the main LR, `lm_head` and `embed_tokens` in `target_modules`, `use_rslora=True` at high ranks — are CPT-specific decisions, not tutorial defaults.

## Other public projects

[**MiniRag-Reranker**](https://github.com/mitanshu-2004/MiniRag-Reranker) — hybrid retrieval + a learned reranker over industrial-safety PDFs. The first release had a circular evaluation (trained and tested on the same eight questions). The current README walks through what was wrong and what the actual held-out numbers look like (NDCG@5: 0.59 baseline → 0.70 learned).

[**RAG-assistant**](https://github.com/mitanshu-2004/RAG-assistant) — Llama 3.3 70B over policy documents, but most of the work went into a Pydantic schema with a `model_validator` that refuses to parse "Fully Answered" responses with empty citations. 0 hallucinated responses on a 9-question eval.

[**Churn / RetainIQ**](https://github.com/mitanshu-2004/Churn) — Cox proportional hazards on Steam reviews, augmented with six LLM-extracted risk signals. 5-fold CV C-index 0.60 → 0.87. The README states clearly that part of the lift may reflect the LLM reading the recommendation label out of the review text.

[**Primetrade-Analysis**](https://github.com/mitanshu-2004/Primetrade-Analysis) — trader segmentation, plus a post-mortem on two follow-on prediction models that didn't work. The post-mortem is the more useful half.

[**chess**](https://github.com/mitanshu-2004/chess) ([chesstra.vercel.app](https://chesstra.vercel.app)) — multiplayer chess on Firestore with version-counter dedup, presence heartbeat, throttled timer writes, and a separate Stockfish backend.

[**portfolio**](https://github.com/mitanshu-2004/portfolio) ([mitanshu.me](https://mitanshu.me)) — Next.js 15 with a Groq-backed chatbot grounded against `lib/knowledge.ts`. Multi-key client that parks rate-limited keys per Groq's 429 hint.

## Looking for

Full-time Robotics SWE, Research Engineering, ML Engineering, or Applied / Foundation-Model AI roles starting June 2026. Internships and short contracts available immediately. Open to relocation.

[mitanshu.me](https://mitanshu.me) · [LinkedIn](https://linkedin.com/in/mitanshugoel) · [Hugging Face](https://huggingface.co/mitanshugoel) · mitanshug2004@gmail.com

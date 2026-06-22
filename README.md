
# Mitanshu Goel

**Robotics & Physical AI Engineer.** I build VR teleoperation, real-time robot control, and the robot-learning
data pipelines behind them. I also build RAG/LLM systems and ML I can defend, where the eval comes before the number.

🌐 [mitanshu.me](https://mitanshu.me) · 💼 [LinkedIn](https://linkedin.com/in/mitanshugoel) · ✉️ mitanshug2004@gmail.com

B.Tech ECE (minor in AI & ML), 2026. I just finished a robotics + physical-AI internship: VR teleoperation on real
Elite CS66 and Franka FR3 arms, multi-sensor capture, and an imitation-learning dataset. Open to Robotics Software,
Physical AI, and ML roles (India / India-friendly remote).

---

### Selected projects

| Project | What it is |
|---|---|
| [**RAG-assistant**](https://github.com/mitanshu-2004/RAG-assistant) | Grounded policy Q&A (Llama 3.3 70B) that abstains when retrieval comes back empty, enforces a citation on every answer through a Pydantic contract, and retries on invalid output. 0 hallucinations / 8-of-9 answerability on a held-out rubric. |
| [**llm-survival-churn**](https://github.com/mitanshu-2004/llm-survival-churn) | Cox proportional-hazards churn study on ~10K Steam reviews. The real result was a leakage audit that cut a flashy +0.26 C-index gain down to an honest +0.14, guarded by a contract test. |
| [**MiniRag-Reranker**](https://github.com/mitanshu-2004/MiniRag-Reranker) | Hybrid PDF retrieval (dense + BM25, 2,570 chunks) with score-gated abstention on FastAPI. After catching train/test leakage I rebuilt the eval on a disjoint held-out set, scored at the document level so a retriever can't game it. |
| [**chess (Chesstra)**](https://github.com/mitanshu-2004/chess) · [live](https://chesstra.vercel.app) | React 19 browser chess with a Firestore multiplayer sync protocol: versioned idempotent writes, heartbeat presence, throttled clock writes, opponent-side end-state recovery. |
| **Reddit continued-pretraining** · [models](https://huggingface.co/mitanshugoel) | Trained a small transformer from scratch and QLoRA-fine-tuned Qwen2.5-3B with a custom two-GPU (DDP) loop: token-offset sharding and checkpoint resume by token budget across Colab/Kaggle sessions. |
| [**Hexapod**](https://github.com/atom-robotics-lab/Hexapod) (team) | 18-DOF hexapod in ROS 2 + Gazebo. My part: the tripod-gait controller (/cmd_vel to per-leg foot targets) and the analytic law-of-cosines leg inverse-kinematics. |

---

### Tech

**Languages:** Python · C++ · JavaScript / TypeScript · SQL
**Robotics:** ROS 2 · ros2_control · MoveIt · real-time C++ control · inverse kinematics · SE(3) transforms · VR teleoperation (Quest 3) · RealSense / RGB-D · multi-sensor sync · LeRobot · Gazebo
**ML / LLM:** PyTorch · RAG (hybrid retrieval) · QLoRA / PEFT · sentence-transformers · ChromaDB · YOLOv8 · OpenCV · scikit-learn · lifelines (survival analysis) · held-out evaluation
**Tools:** FastAPI · SQLite (FTS5) · Hugging Face Hub · Git · Linux

<!-- Optional GitHub stats widget — uncomment to show:
![Mitanshu's GitHub stats](https://github-readme-stats.vercel.app/api?username=mitanshu-2004&show_icons=true&hide_border=true)
-->

<!--
  GITHUB PROFILE README (paste-ready)
  ===================================
  Where this goes: the special repo github.com/mitanshu-2004/mitanshu-2004
  (same name as your username). Put this content in its README.md, on the
  default branch. It renders at the top of your GitHub profile.

  Recommended pinned repos (set these in the GitHub UI: profile > Customize your pins).
  These are your strongest, non-liability repos:
    1. atom-robotics-lab/Hexapod   (your ros2_control + URDF work)
    2. RAG-assistant               (Pydantic-guarded, 0 hallucinations)
    3. MiniRag-Reranker            (held-out eval after catching leakage)
    4. llm-survival-churn          (leakage decomposition)
    5. chess                       (live multiplayer, chesstra.vercel.app)
    6. Stock-Influence             (deployed full-stack, live demo)
  Avoid pinning StockMetrics or memory-assistant as headline proof (known caveats).

  Everything below this comment is the README. Delete this comment block if you want.
-->

# Mitanshu Goel

Robotics and Physical AI engineer. ECE new-grad from MAIT Delhi (2026). Most of my work sits where hardware meets learned models, with a habit underneath all of it: build the eval before you trust the number.

Right now I am at **nFerent.ai**, building a bimanual VR teleoperation rig. A Meta Quest 3 drives a pair of Elite Robots CS66 arms through a real-time C++ control loop, and the same loop extends to a Franka Research 3 so it covers both arm families. The rig also collects the data it runs on: every session logs synchronised arm state, headset pose, and multi-camera capture that downstream imitation-learning policies train on.

## What I work on

- **Real-time robotics.** C++ control loops on industrial arms, ROS 2 and ros2_control, MoveIt, Cartesian servoing, teleoperation safety stacks, inverse kinematics.
- **Robot learning data.** Multi-sensor capture synchronised on one hardware clock, with watchdogs that catch the quiet failures (a camera silently repeating a frame under load).
- **Foundation models.** Six continued-pretraining runs on a Reddit corpus I scraped and processed myself: Mistral 7B at two ranks, Qwen 2.5 at three scales, and a nanoGPT built from scratch.
- **Applied ML and LLMs.** Retrieval with held-out evaluation, Pydantic-guarded grounded Q&A, survival analysis, and a few honest failure write-ups.

## Selected projects

- **Bimanual VR teleoperation (nFerent.ai)** is a real-time C++ stack that drives two Elite CS66 arms, extended to a Franka FR3, with One-Euro filtering, SE(3) smoothing, and singularity and step-cap guards. Company work, no public repo.
- **[Hexapod](https://github.com/atom-robotics-lab/Hexapod)** is an 18-DoF hexapod in ROS 2 and Gazebo. I wrote the URDF xacro and the full ros2_control hardware interface. The gait and analytic IK were a teammate's.
- **[RAG-assistant](https://github.com/mitanshu-2004/RAG-assistant)** is grounded policy Q&A where a Pydantic validator rejects "Fully Answered" replies that have no citations, at parse time. It returned 0 hallucinations on a 9-question held-out rubric.
- **[MiniRag-Reranker](https://github.com/mitanshu-2004/MiniRag-Reranker)** is hybrid retrieval over industrial-safety PDFs. I caught that the original eval reused the training questions and rebuilt it around a disjoint held-out set with NDCG, MRR, and Recall@k.
- **[llm-survival-churn](https://github.com/mitanshu-2004/llm-survival-churn)** is a Cox survival model whose real contribution was a leakage decomposition. Most of the headline lift re-encoded the label, so I kept the roughly +0.14 that actually looks forward and added a contract test to stop the leak coming back.
- **[Chesstra](https://github.com/mitanshu-2004/chess)** is real-time multiplayer chess on Firestore with a versioned sync protocol and opponent-side end-state recovery. It is live at [chesstra.vercel.app](https://chesstra.vercel.app).

## Stack

`C++` `Python` `TypeScript` · ROS 2, ros2_control, MoveIt, real-time Linux, Elite CS SDK, Franka libfranka · PyTorch, Unsloth, PEFT and LoRA (rsLoRA), Hugging Face · FastAPI, ChromaDB, Sentence-Transformers, Pydantic · lifelines, scikit-learn, XGBoost · Next.js, React, Firestore

## Reach me

Portfolio [mitanshu.me](https://mitanshu.me) · Email mitanshug2004@gmail.com · [LinkedIn](https://linkedin.com/in/mitanshugoel)

Open to full-time roles in Physical AI, Robotics SWE, ML Engineering, and Research Engineering. Based in Delhi, open to relocation.

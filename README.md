<!--
  GITHUB PROFILE README (paste-ready)
  ===================================
  Where this goes: the special repo github.com/mitanshu-2004/mitanshu-2004
  (same name as your username). Put this content in its README.md, on the
  default branch. It renders at the top of your GitHub profile.

  Recommended pinned repos (set these in Profile > Customize your pins).
  Recruiters click through pins, so these are your strongest, non-liability repos:
    1. atom-robotics-lab/Hexapod   (your ROS 2 control node + ros2_control work)
    2. RAG-assistant               (Pydantic-guarded, 0 hallucinations on the eval)
    3. MiniRag-Reranker            (rebuilt the eval after catching leakage)
    4. llm-survival-churn          (leakage decomposition)
    5. chess                       (live multiplayer, chesstra.vercel.app)
    6. Stock-Influence             (deployed full-stack, live demo)
  Do NOT pin StockMetrics or memory-assistant as headline proof (known caveats).

  Everything below this comment is the README. Delete this comment block if you want.
-->

# Mitanshu Goel

Robotics and Physical AI engineer. ECE new-grad from MAIT Delhi (2026). Most of my work sits where hardware meets learned models, with one habit underneath it: build the eval before you trust the number.

Right now I am at **nFerent.ai**, building a bimanual VR teleoperation rig and the data pipeline around it. A Meta Quest 3 drives a pair of Elite Robots CS66 arms through a real-time C++ control loop, and the same loop extends to a Franka Research 3 so it covers both arm families. The rig is also how the data gets made: every session records synchronised arm state, headset pose, and multi-camera RGB-D as episodes for imitation learning, and a separate capture tool puts two MANUS gloves and three RealSense cameras on one hardware clock.

## What I work on

- **Real-time robotics.** C++ control loops on industrial arms (SCHED_FIFO, memory locked, CPU pinned), ROS 2 and ros2_control, MoveIt, Cartesian servoing, VR teleoperation, inverse kinematics, and the safety stacks that keep an arm from hurting itself.
- **Robot-learning data.** Multi-sensor capture synchronised on one hardware clock, with a watchdog that catches the quiet failures, like a camera silently repeating a frame under load.
- **Foundation models.** Continued pretraining on a Reddit corpus I scraped and cleaned myself, including a distributed training loop I wrote by hand that resumes from the exact token after a dropped cloud session.
- **Applied ML and LLMs.** Retrieval with held-out evaluation, Pydantic-guarded grounded Q&A, survival analysis, and a few honest failure write-ups.

## Selected projects

- **Bimanual VR teleoperation (nFerent.ai)** is a real-time C++ stack that drives two Elite CS66 arms, extended to a Franka FR3, with One-Euro filtering, SE(3) smoothing, and singularity and step-cap guards. Company work, no public repo.
- **[RAG-assistant](https://github.com/mitanshu-2004/RAG-assistant)** is grounded policy Q&A where a Pydantic validator rejects answers that claim completeness without citations, at parse time. It returned 0 hallucinations on a 9-question held-out rubric.
- **[MiniRag-Reranker](https://github.com/mitanshu-2004/MiniRag-Reranker)** is hybrid retrieval over industrial-safety PDFs. I caught that the original eval reused the training questions and rebuilt it around a disjoint held-out set with NDCG, MRR, and Recall@k. Measured that way the learned reranker did not clearly beat the plain hybrid baseline, and the corrected eval is the point.
- **[llm-survival-churn](https://github.com/mitanshu-2004/llm-survival-churn)** is a Cox survival model whose real contribution is a leakage decomposition. Most of the headline C-index lift re-encoded the label, so I kept the roughly +0.14 that actually looks forward and added a contract test to stop the leak coming back.
- **[Hexapod](https://github.com/atom-robotics-lab/Hexapod)** is an 18-DoF hexapod in ROS 2 and Gazebo, built with A.T.O.M. Robotics. I worked on the control side: the tripod-gait and analytic-IK node, the ros2_control hardware interface, and the launch wiring. The URDF is CAD-exported. Team project, simulation only.
- **[Chesstra](https://github.com/mitanshu-2004/chess)** is real-time multiplayer chess on Firestore with a versioned sync protocol and opponent-side end-state recovery. It is live at [chesstra.vercel.app](https://chesstra.vercel.app).

## Stack

`C++` `Python` `TypeScript` · ROS 2, ros2_control, MoveIt, real-time Linux, Elite CS SDK, Franka libfranka · PyTorch, Unsloth, PEFT and LoRA (rsLoRA), accelerate (DDP), Hugging Face · FastAPI, ChromaDB, Sentence-Transformers, Pydantic · lifelines, scikit-learn, XGBoost · Next.js, React, Firestore

## Reach me

Portfolio [mitanshu.me](https://mitanshu.me) · Email mitanshug2004@gmail.com · [LinkedIn](https://linkedin.com/in/mitanshugoel)

Open to full-time roles in Physical AI, Robotics SWE, ML Engineering, and Research Engineering. Based in Delhi, open to roles across India and remote roles that work with India hours.

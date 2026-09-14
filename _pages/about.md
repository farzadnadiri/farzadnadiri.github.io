---
permalink: /
title: "Farzad Nadiri - Perception & Physical AI"
author_profile: true
classes: wide
redirect_from:
  - /about/
  - /about.html
---

Hi there 👋 I am Farzad,

I am a perception and physical AI engineer with a PhD research track in autonomous driving at Simon Fraser University and more than a decade of shipping production software. I build bird's eye view camera perception, IMU and camera sensor fusion for localization, and vision based lateral control, validated both in CARLA and on physical robots.

I like turning research into systems that actually run. Alongside my research I architect large scale ML inference pipelines on AWS SageMaker, and earlier in my career I worked in the team that won the RoboCup 2015 Teen Size humanoid world championship. I enjoy working end to end, from data and modeling to deployment and monitoring, and I care about clear communication, collaboration, and measurable outcomes.

Let us connect and build something impactful together!

## Current roles

- Senior Software and ML Engineer, Quartech
- PhD Student, Mechatronic Systems Engineering, AI and Robotics, Simon Fraser University
- Research Assistant, Autonomous and Intelligent Systems Lab, SFU

## Focus areas

- Camera and multi sensor perception for autonomous driving and robotics
- Sensor fusion, localization, and control under real world uncertainty
- Vision language models and agentic architectures for driver assistance
- Design and deployment of cloud based, production grade ML services

## Core skills

- **Perception and sensor fusion**: 2D and 3D detection and tracking, semantic scene understanding, camera calibration, homography and bird's eye view transforms, IMU and camera fusion, 3D point cloud localization, lane and obstacle perception, multi rate sensor synchronization, CARLA, CAN and OBD-II with DBC decoding
- **Deep learning**: PyTorch, CNNs, Vision Transformers, temporal transformers, cross attention multimodal fusion, vision foundation models, vision language models, LLMs and RAG, class imbalanced evaluation with UAR, subject wise cross validation, ablation design
- **Production ML and infrastructure**: AWS SageMaker for training, batch inference and endpoints, MLflow tracking and model registry, S3, large scale image and sensor log pipelines, dataset curation, automated label QC and scoring, Docker, GitHub Actions CI/CD, CUDA and GPU serving, vLLM, Azure ML, OpenShift AI
- **Languages and tooling**: Python, C#, C, C++, TypeScript, Java, SQL, NumPy, Pandas, OpenCV, Hugging Face Transformers, python-can, cantools, pytest, ruff and mypy, Git

## Work experience

- **Senior Software and ML Engineer**, Quartech, Oct 2023 to Present, Vancouver, Canada

  *Digital pathology quality control AI, Provincial Health Services Authority*

  - Led the AI solution for an offline, cloud scale visual inspection pipeline over gigapixel imagery on AWS SageMaker, covering S3 ingestion, tiling, embedding extraction with transformer based vision foundation models, batched inference orchestration, result aggregation, and QC scoring
  - Benchmarked two pathology foundation models against lightweight and fine tuned classification heads on accuracy, throughput, and cost, quantifying cross scanner generalization before committing to a production configuration
  - Defined tile level quality metrics and automated scoring to measure generated label quality against expert review, and built coverage aware heatmap overlays so model output stayed interpretable and auditable for reviewers at scale
  - Stood up MLflow experiment tracking and a model registry around SageMaker training jobs so runs, datasets, and artifacts stayed reproducible, and models were promoted through a versioned registry rather than ad hoc checkpoints

  *Court session transcription AI, BC Court Systems*

  - Fine tuned Whisper for courtroom audio covering legal terminology, overlapping speakers, and far field recording, and shipped it as a privacy preserving, self hosted GPU and CUDA deployment inside the ministry environment
  - Designed a case aware context refinement layer in which an LLM post processes the transcript against party names, statutes, and matter records, correcting proper nouns and citations that acoustic decoding alone gets wrong

  *Early Childhood Education Registry, BC Ministry of Education and Childcare*

  - Led backend development of a province wide certification platform, integrating with government systems and shipping through GitHub Actions CI/CD into containerized OpenShift deployments, with accessibility and security compliance

- **Senior Software Engineer**, Pacific Blue Cross, Jan 2023 to Jul 2023, Vancouver, Canada

  - Raised throughput of a data mapping platform serving one million users by about 25 percent through service oriented architectural refactoring and automated test coverage, and authored migration tooling across legacy databases
  - Enhanced scalability and reliability by improving monitoring, refining data access patterns, and collaborating with cross functional teams on incident response and performance tuning

- **Software Engineering Team Lead**, Metalive, Dec 2020 to Dec 2022, Tehran, Iran

  - Led a team delivering a multi role WebRTC telemedicine platform during COVID-19, with peer to peer video consultations, scheduling, and electronic prescriptions, and owned the architecture and release process
  - Applied computer vision models to detect low quality video frames during teleconsultations, and contributed to streaming and VOD pipelines built on WebRTC, FFmpeg, and HLS

- **Software Engineer**, Parsertebat, Jun 2016 to Dec 2020, Tehran, Iran

  - Built server side, monitoring, and embedded software for an OBD-II and IoT telematics product that fused vehicle bus and auxiliary sensor streams to characterize driving behavior and price usage based insurance premiums
  - Led design and development of a high traffic wagering platform from scratch, growing it to more than 70k users and 32M dollars in annual revenue under peak event load

## Research experience

- **Research Assistant**, Autonomous and Intelligent Systems Lab, SFU, May 2024 to Present, Vancouver, Canada  
  Supervisor, Professor Ahmad B. Rad, [link](https://www.sfu.ca/fas/schools/mechatronic-systems-engineering/faculty/faculty-members/arad.html)

  - Built DriveMCP, an agentic driver assistance architecture that decomposes a monolithic vision language driving assistant into specialized experts exposed as Model Context Protocol servers, covering traffic rule retrieval, weather and traction reasoning, and CAN and OBD vehicle health, coordinated by a stateful orchestration graph at sub second advisory latency
  - Grounded it in a CARLA camera and LiDAR perception stack with RGB detection, range refinement, and Kalman tracking, feeding a typed world state with per field confidence, gated through an RSS and TTC based safety arbiter, and evaluated against VLM direct, RAG, and no arbiter baselines under injected perception and CAN faults
  - Open sourced MCP-CAN, the telemetry server in this stack, with live CAN and OBD-II decoding via cantools, a virtual CAN backend, and a multi ECU simulator so it runs without hardware
  - Built a four class driver impairment classifier on the Toyota Research Institute Impaired Driving Dataset, fusing gaze, vehicle dynamics, and video through a temporal transformer with cross attention fusion, with multi rate synchronization to 10 Hz, explicit missingness encoding, and UAR reported under subject wise folds
  - Designed and published a look down lane perception and lateral control system using a homography based bird's eye view transform, holding accuracy on uphill, downhill, and curved geometry where look ahead methods degrade
  - Developed an IMU and camera sensor fusion localization method that compensates perspective distortion under body tilt, reducing position estimation error in landmark sparse environments and on physical hardware

- **Research Assistant**, Autonomous Robots Lab, Team Parand, Jan 2011 to May 2016, Tehran, Iran  
  Kid Size (50 cm) and Teen Size (100 cm) 20 DOF humanoid robots, built from scratch

- Designed and implemented the vision pipeline for object detection and tracking on humanoid robots, including color segmentation, feature extraction, and object classification.

- Developed the soccer behavior layer with field localization, obstacle avoidance, and team tactics, connecting perception to decision making and motion control.

- Implemented multi robot UDP communication for cooperation and coordination between agents, including message formats and synchronization strategies.

- Built and maintained multithreaded modules, such as the omnidirectional bipedal walk engine, I and O, motion designer, and balance control components.
## Selected projects and code

- **DriveMCP, agentic driver assistance**  
  An MCP powered architecture that splits a vision language driving assistant into specialized expert servers behind a stateful orchestration graph, grounded in a CARLA camera and LiDAR perception stack and gated by an RSS and TTC safety arbiter. Under review at IEEE Transactions on Intelligent Vehicles.

- **MCP-CAN, vehicle telemetry over MCP**  
  Open source Model Context Protocol server for live CAN and OBD-II decoding with cantools, including a virtual CAN backend and a multi ECU simulator so it runs with no hardware attached, [Code](https://github.com/farzadnadiri/MCP-CAN)

- **DriverStateNet, multimodal driver impairment classification**  
  Four class driver state classifier over the Toyota Research Institute Impaired Driving Dataset, fusing gaze, vehicle dynamics, and video with a temporal transformer and cross attention fusion, synchronized to 10 Hz with explicit missingness encoding and evaluated by UAR under subject wise folds, [Code](https://github.com/farzadnadiri/DriverStateNet)

- **Look down lane perception and lateral control**  
  Homography based bird's eye view lane perception and lateral control for autonomous vehicles, evaluated in CARLA across uphill, downhill, and curved road geometry where look ahead configurations lose accuracy, [Paper](https://www.mdpi.com/2075-1702/13/3/211)

- **IMU and camera fusion for localization**  
  Sensor fusion method that compensates perspective distortion under body tilt to improve position estimation in landmark sparse environments, validated on physical humanoid hardware, [Paper](https://link.springer.com/article/10.1007/s41315-025-00451-5), [Code](https://github.com/farzadnadiri/AccurateBirdEyeView)

- **Modular humanoid soccer software framework**  
  Modular software stack for humanoid soccer robots covering vision, behavior, localization, and motion, used on Teen Size and Kid Size platforms in RoboCup and IranOpen competitions, [Code](https://github.com/farzadnadiri/HumanoidSoccerRobot)

## Education

- PhD, Mechatronic Systems Engineering, AI and Robotics, Simon Fraser University, May 2024 to Present, Vancouver, Canada  
  Research, perception and control for autonomous systems, sensor fusion and localization, agentic architectures for driver assistance, simulation to real validation using CARLA and physical platforms

- M.Sc., Computer Science, AI and Robotics, Science and Research University, 2020, Tehran, Iran  
  Thesis, A Fusion of Inertial Measurement Unit Data and Bird's Eye View Perspectives, focused on improving localization accuracy through sensor fusion, Best Master Thesis Award, [Code](https://github.com/farzadnadiri/AccurateBirdEyeView)

- B.Eng., Information Technology, Azad University, Parand Branch, 2014, Tehran, Iran  
  Final project, Modular Software Framework for Humanoid Soccer Robots, including perception, behavior, localization, and motion modules, [Code](https://github.com/farzadnadiri/HumanoidSoccerRobot)

## Honors and awards

- Special Graduate Dean's Entrance Scholarship, Simon Fraser University, 44k CAD
- RoboCup 2015 Teen Size World Champion
- Supported by the National Elites Foundation of Iran, 2020 to 2022
- Best Master Thesis Award, Science and Research University, 2020
- Best Student Research Award, four consecutive years, Research Week, 2011 to 2015, Tehran, Iran
- Referee Committee Member, ICT Challenge national competitions, Sharif University, Jul 2020, [link](https://ictchallenge.ir/ictchallenge5/)

- RoboCup, Teen Size Humanoid

  - World Championship, RoboCup 2015, Hefei, China, [link](https://farzadnadiri.github.io/images/robocup_2015.jpg)
  - 3rd Place, RoboCup 2014, João Pessoa, Brazil, [link](https://farzadnadiri.github.io/images/robocup_2014.jpg)
  - Championship, IranOpen International Competitions 2015, Tehran, [link](https://farzadnadiri.github.io/images/io_teen_2015.jpg)
  - Championship, IranOpen International Competitions 2013, Tehran, [link](https://farzadnadiri.github.io/images/io_teen_2013.jpg)

- RoboCup, Kid Size Humanoid
  - 2nd Place, IranOpen International Competitions 2016, Tehran, [link](https://farzadnadiri.github.io/images/io_kid_2016.jpg)
  - Championship, IranOpen International Competitions 2015, Tehran, [link](https://farzadnadiri.github.io/images/io_kid_2015.jpg)

## Journal reviewing

- Nature, Scientific Reports, Aug 2025 to Present, Vancouver, Canada, [link](https://www.nature.com/srep)
- Springer, Computational Intelligence Systems, Sep 2025 to Present, Vancouver, Canada, [link](https://link.springer.com/journal/44196)
- Springer, Cognitive Computation, Feb 2025 to Present, Vancouver, Canada, [link](https://link.springer.com/journal/12559)
- Springer, Supercomputing, Feb 2025 to Present, Vancouver, Canada, [link](https://link.springer.com/journal/11227)
- Springer, Discover Applied Sciences, Feb 2025 to Present, Vancouver, Canada, [link](https://link.springer.com/journal/42452)
- Springer, Discover Artificial Intelligence, Feb 2025 to Present, Vancouver, Canada, [link](https://link.springer.com/journal/44163)
- International Journal of Humanoid Robotics, Aug 2025 to Jan 2026, Vancouver, Canada, [link](https://www.worldscientific.com/worldscinet/IJHR)
- COJ Robotics and Artificial Intelligence, COJRA, Jul 2025 to Jan 2026, Vancouver, Canada, [link](https://access.portico.org/Portico/loviView?cs=ISSN_28324463_1848&content=E-Journal%20Content)

## Certifications

- PyTorch: Fundamentals, [link](https://coursera.org/share/407bdacac3092e1240aa0163b8cc9987)
- Hyperparameter Tuning, Regularization and Optimization, [link](https://coursera.org/share/cd6fff206a940286d4c91cbb7d124b86)
- Machine Learning Specialization, [link](https://coursera.org/share/0a31b713130f0f45668cf8692ee5c786)
- Structuring Machine Learning Projects, [link](https://coursera.org/share/611bf132c430828ca253cd9326d20e2d)
- Improving Deep Neural Networks, [link](https://coursera.org/share/cd6fff206a940286d4c91cbb7d124b86)
- Neural Networks and Deep Learning, [link](https://coursera.org/share/c9823dffe232597e18a301cc77259f94)
- Unsupervised Learning, Recommenders, and Reinforcement Learning, [link](https://coursera.org/share/abe106fa9d91831501c14443d047922e)
- Convolutional Neural Networks, [link](https://coursera.org/share/fa16eec8c25de902a78fdb43981fd024)
- Supervised Machine Learning, Regression, and Classification, [link](https://coursera.org/share/2dfdfa80f779f3a0ef5b43763a6087dc)
- Advanced Learning Algorithms, [link](https://coursera.org/share/d22d27147e47722a77b9c263b2dc61d3)
- International Spring School on humanoid soccer robots, [link](https://farzadnadiri.github.io/images/humanoid_school.jpg)

## Volunteering

- Teaching Assistant, Azad University, Apr 2011 to Jun 2012, Tehran, Iran

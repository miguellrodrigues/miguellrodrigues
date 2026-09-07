# miguel l. rodrigues

**computer vision · control systems · industrial AI**  
Digimet Solutions · CEFET-MG · Divinópolis, Brazil

**→ [miguellrodrigues.github.io](https://miguellrodrigues.github.io)** — portfolio, case studies and papers

---

I build computer-vision systems for industrial inspection and field imagery — segmentation, keypoint detection, and the inference pipelines that run them in production. Alongside that, I research event-triggered control of LPV systems under actuator saturation.

```python
me = {
    "work":     ["segmentation", "keypoint detection", "ONNX / INT8 inference", "AWS deployment"],
    "research": ["event-triggered control", "LPV systems", "actuator saturation"],
    "else":     ["chess", "poetry", "music"],
}
```

---

**vision & AI**  
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![ONNX](https://img.shields.io/badge/ONNX-005CED?style=flat-square&logo=onnx&logoColor=white)

**infra & languages**  
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![C](https://img.shields.io/badge/C-00599C?style=flat-square&logo=c&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)

**embedded**  
![STM32](https://img.shields.io/badge/STM32-03234B?style=flat-square&logo=stmicroelectronics&logoColor=white)
![ESP32](https://img.shields.io/badge/ESP32-E7352C?style=flat-square&logo=espressif&logoColor=white)

---

**systems**

Applied work, written up as case studies on the [portfolio](https://miguellrodrigues.github.io).

### [coffeevision](https://github.com/miguellrodrigues/coffeevision)
> Maps coffee ripeness from field photographs into H3 cells, colouring a cell only above a minimum number of photographs.

- Detection over 216 field photographs, 5,849 fruit detections
- H3 geospatial aggregation at 57 m cell size, 5.5 m median GPS accuracy
- PyTorch · FastAPI · PostGIS · React
- [case study](https://miguellrodrigues.github.io/work/coffeevision/)

### weld bead inspection · Digimet Solutions
> Segmentation and keypoint models that measure weld bead geometry from field images, running unattended in production.

- End to end — annotation, training, validation, post-processing, deploy
- Serverless inference on AWS Lambda with CloudWatch monitoring
- ONNX export and INT8 quantization for latency and cost
- Proprietary — no public repo · [case study](https://miguellrodrigues.github.io/work/weld-bead/)

### [gridcast](https://github.com/miguellrodrigues/gridcast)
> Day-ahead electricity demand forecasting with leakage-safe walk-forward validation, and an ablation measuring what a weather feed adds.

- 1.8% day-ahead MAPE, 46% better than the previous-day baseline
- Weather information accounts for 1.1% of the error
- LightGBM · scikit-learn · pandas · pytest
- [case study](https://miguellrodrigues.github.io/work/gridcast/)

---

**libraries**

Open-source libraries from different parts of my academic work — robotics, structural mechanics, control theory and embedded systems.

### [robotic_tools](https://github.com/miguellrodrigues/robotic_tools)
> Symbolic and numerical robot analysis from Denavit–Hartenberg parameters.

- Forward and inverse kinematics, position and orientation
- Forward dynamics via Euler–Lagrange equations
- Jacobian computation and inverse velocity kinematics
- Gradient descent and evolutionary IK solvers
- Works with any serial manipulator — plug in the DH table

### [beam_tools](https://github.com/miguellrodrigues/beam_tools)
> Symbolic Euler–Bernoulli beam analysis using Macaulay singularity functions and SymPy.

- Closed-form shear force, bending moment, slope and deflection
- Statically determinate and indeterminate (hyperstatic) beams
- Point loads, uniform and triangular distributed loads, applied moments
- Fixed, hinged and roller supports with automatic compatibility equations
- Fully symbolic — substitute numerical values at any stage

### [prometheus](https://github.com/miguellrodrigues/prometheus)
> ESP32 closed-loop temperature controller with MQTT telemetry, built with UFMG's GREA research group.

- 2nd-order IIR pre-filter and discrete PID with anti-windup and output saturation
- Switches from open-loop warm-up to closed loop near the setpoint
- DS18B20 1-Wire sensing, MCPWM actuation at ~1.2 kHz
- MQTT telemetry with remote setpoint and config updates, no reflashing
- Dual-core FreeRTOS — control loop on core 0, MQTT on core 1
- Configuration persisted on SPIFFS

### [fpwm-signal-generator](https://github.com/miguellrodrigues/fpwm-signal-generator)
> Function generator on ESP32.

- Sine, sawtooth, triangle and square waveforms via PWM and hardware timers
- Frequency error under 1% across the tested range
- Buttons and a 16x2 LCD for the physical interface
- Runs on a custom development board (Prometheus) of my own design
- C, ESP-IDF

---

**research**

Theory and design of **event-triggered control systems** for uncertain and nonlinear plants, with emphasis on **Linear Parameter Varying (LPV)** models and **robust control** under actuator saturation.

Current topics:
- Periodic event-triggered control with co-design via evolutionary optimization
- Dynamic and adaptive event generators for transmission reduction
- LPV systems with saturation constraints

> M.Sc. in Electrical Engineering · CEFET-MG · 2025–2027

**publications**

- **Gerador de Eventos Adaptativo com Rastreamento de Função Hazard para Sistemas LPV Saturantes**  
  Rodrigues, Silva, Leite · *CBA 2026* · [pdf](https://miguellrodrigues.github.io/papers/CBA_ETM_HAZARD.pdf)

- **Co-Design and Evolutionary Optimization of Periodic Event-Triggered Robust Control for LPV Systems**  
  Oliveira, Rodrigues, Guelton, Motchon, Leite · *ROCOND 2025* · [pdf](https://miguellrodrigues.github.io/papers/ROCOND25_Robust_and_ETM.pdf)

- **Gerador Dinâmico de Eventos com Tratamento de Ruído para Redução de Transmissões**  
  Rodrigues, Silva, Leite · *SBAI 2025* · [pdf](https://miguellrodrigues.github.io/papers/SBAI_SBSE_ETC_MIGUEL.pdf)

- **Gerador de Eventos para Minimização de Transmissões em Sistemas LPV Saturantes**  
  Rodrigues, Silva, Leite · *CBA 2024* · [pdf](https://miguellrodrigues.github.io/papers/CBA_ETC_MIGUEL.pdf)

- **Modelagens e Simulações Computacionais Aplicadas ao Desenvolvimento Remoto de Sistemas Mecatrônicos**  
  Silva, Alves, Rodrigues, Dâmaso · *CBA 2022* · [pdf](https://miguellrodrigues.github.io/papers/CBA22_REMOTE_MECHATRONICS.pdf)

---

<p align="center">
  <img src="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=miguellrodrigues&theme=tokyonight" />
  <img src="https://github-profile-summary-cards.vercel.app/api/cards/stats?username=miguellrodrigues&theme=tokyonight" />
</p>

<p align="center">
  <img src="https://github-readme-streak-stats-eight.vercel.app?user=miguellrodrigues&theme=tokyonight&hide_border=true" />
</p>

---

[![Portfolio](https://img.shields.io/badge/Portfolio-24594D?style=flat-square&logo=githubpages&logoColor=white)](https://miguellrodrigues.github.io)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/miguellr16/)
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:miguel.lukas52@gmail.com)

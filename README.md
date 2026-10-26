```html
<div align="center">

# ⚛️ PHYSIOPT-X

### PHYSICS-AWARE SELF-VERIFYING OPTIMIZATION & CONTROL

**Autonomous Systems • Physics Consistency • Fault Diagnosis • Intelligent Control**

![MATLAB](https://img.shields.io/badge/PLATFORM-MATLAB%20%2F%20SIMULINK-00D4FF?style=for-the-badge&logo=mathworks&logoColor=white)
![Control](https://img.shields.io/badge/DOMAIN-ADVANCED%20CONTROL-7B61FF?style=for-the-badge)
![Physics](https://img.shields.io/badge/ENGINE-PHYSICS--AWARE-00E5A8?style=for-the-badge)
![Research](https://img.shields.io/badge/LEVEL-RESEARCH%20FRAMEWORK-FFB547?style=for-the-badge)
![Systems](https://img.shields.io/badge/SYSTEM-CYBER--PHYSICAL-FF5370?style=for-the-badge)

**MODEL ≠ REALITY**

*When the physical system disagrees with its model, intelligence begins.*

</div>

---

<div align="center">

<img
  src="https://capsule-render.vercel.app/api?type=rect&height=8&color=0:00F0FF,45:755CFF,100:00E5A8"
  width="100%"
  alt="PHYSIOPT-X gradient divider"
/>

</div>

<h1 align="center">
  PHYSICS-AWARE INTELLIGENT CONTROL
</h1>

<p align="center">
  <strong>
    A Self-Verifying Optimization and Fault-Tolerant Control Framework
    for Autonomous Cyber-Physical Systems
  </strong>
</p>

<div align="center">

<a href="#project-overview">PROJECT OVERVIEW</a>
&nbsp; ◆ &nbsp;
<a href="#system-architecture">SYSTEM ARCHITECTURE</a>
&nbsp; ◆ &nbsp;
<a href="#physics-verification">PHYSICS VERIFICATION</a>
&nbsp; ◆ &nbsp;
<a href="#optimization-and-control">OPTIMIZATION</a>
&nbsp; ◆ &nbsp;
<a href="#getting-started">GET STARTED</a>

</div>

<br/>

<!-- ====================================================== -->
<!-- HERO ANIMATION                                         -->
<!-- ====================================================== -->

<div align="center">

<img
  src="assets/physioptx-hero.gif"
  width="100%"
  alt="PHYSIOPT-X animated physics-aware control and optimization framework"
/>

</div>

<div align="center">

### ◈ OBSERVE → VERIFY → DIAGNOSE → OPTIMIZE → RECOVER ◈

</div>

---

<!-- ====================================================== -->
<!-- PROJECT OVERVIEW                                       -->
<!-- ====================================================== -->

<a id="project-overview"></a>

# ◈ 01 — PROJECT OVERVIEW

**PHYSIOPT-X** is a proposed research framework that combines physical-model consistency verification, fault diagnosis, constrained optimization, and supervisory control for autonomous cyber-physical systems.

The central principle is simple:

> A controller should not blindly trust its internal model. It should continuously evaluate whether the model remains consistent with the behavior of the physical system.

PHYSIOPT-X explores how discrepancies between predicted and observed behavior can support fault detection, diagnosis, controller adaptation, and safe-state decisions.

<div align="center">

| ◈ PHYSICS | ◈ VERIFICATION | ◈ OPTIMIZATION | ◈ RECOVERY |
|:---:|:---:|:---:|:---:|
| Model-based prediction | Residual monitoring | Constrained decisions | Supervisory response |
| Expected behavior | Model vs. reality | Performance vs. limits | Degraded or safe mode |

</div>

---

<!-- ====================================================== -->
<!-- SYSTEM ARCHITECTURE                                    -->
<!-- ====================================================== -->

<a id="system-architecture"></a>

# ◈ 02 — SYSTEM ARCHITECTURE

<div align="center">

<img
  src="https://capsule-render.vercel.app/api?type=rect&height=3&color=0:755CFF,50:00F0FF,100:755CFF"
  width="100%"
  alt="Architecture divider"
/>

</div>

```text
                  PHYSIOPT-X FRAMEWORK
        ┌─────────────────────────────────────┐
        │       PHYSICAL CYBER-SYSTEM         │
        │                                     │
        │   Sensors → Plant → Actuators       │
        └──────────────────┬──────────────────┘
                           │
                           ▼
        ┌─────────────────────────────────────┐
        │        PHYSICS-BASED MODEL          │
        │                                     │
        │   Predict expected system behavior  │
        └──────────────────┬──────────────────┘
                           │
                           ▼
        ┌─────────────────────────────────────┐
        │      CONSISTENCY VERIFICATION       │
        │                                     │
        │   Prediction ↔ Observation          │
        │   Residuals ↔ Thresholds            │
        └──────────────────┬──────────────────┘
                           │
                           ▼
        ┌─────────────────────────────────────┐
        │        FAULT DIAGNOSIS              │
        │                                     │
        │   Normal / Suspected Fault          │
        │   Fault Isolation / Uncertain       │
        └──────────────────┬──────────────────┘
                           │
                           ▼
        ┌─────────────────────────────────────┐
        │      OPTIMIZATION & SUPERVISION     │
        │                                     │
        │   Adapt Controller / Limit Actions  │
        │   Continue / Degrade / Safe Stop    │
        └──────────────────┬──────────────────┘
                           │
                           ▼
        ┌─────────────────────────────────────┐
        │        VERIFICATION & LOGGING       │
        │                                     │
        │   Recheck Response / Record Events  │
        └─────────────────────────────────────┘
```

### SYSTEM DESIGN PRINCIPLE

The framework is designed around a continuous feedback loop rather than a one-time controller calculation.

**Measure → Predict → Compare → Decide → Act → Verify**

---

<!-- ====================================================== -->
<!-- PHYSICS VERIFICATION                                   -->
<!-- ====================================================== -->

<a id="physics-verification"></a>

# ◈ 03 — PHYSICS CONSISTENCY VERIFICATION

The framework compares the measured system response with the response predicted by its physical model.

For a general dynamical system:

<div align="center">

**System Model**

`dx/dt = f(x, u, θ)`

**Prediction Error**

`r(t) = y_measured(t) - y_predicted(t)`

**Verification Decision**

`|r(t)| > threshold → investigate inconsistency`

</div>

Where:

- `x` represents the system state.
- `u` represents the control input.
- `θ` represents model parameters.
- `r(t)` represents the prediction residual.
- `threshold` represents a defined detection limit.

A large residual may indicate a fault, parameter mismatch, disturbance, sensor bias, or unmodeled behavior. It is evidence of inconsistency, not automatic proof of a particular fault.

---

<!-- ====================================================== -->
<!-- OPTIMIZATION AND CONTROL                               -->
<!-- ====================================================== -->

<a id="optimization-and-control"></a>

# ◈ 04 — OPTIMIZATION & INTELLIGENT CONTROL

PHYSIOPT-X investigates how controller decisions can balance tracking performance, control effort, and safe operation.

A general optimization objective can be written as:

<div align="center">

**J = Σ [ q·e²(k) + r·u²(k) ]**

</div>

Subject to system constraints:

<div align="center">

**x(k+1) = f(x(k), u(k), θ)**

**u_min ≤ u(k) ≤ u_max**

**x(k) ∈ X_safe**

</div>

Where:

- `e(k)` is the tracking error.
- `u(k)` is the control input.
- `q` weights tracking performance.
- `r` weights control effort.
- `X_safe` represents the defined safe operating region.

The precise objective function and constraints depend on the selected plant and experimental design.

---

<!-- ====================================================== -->
<!-- OPERATING STATES                                       -->
<!-- ====================================================== -->

# ◈ 05 — SUPERVISORY OPERATING STATES

<div align="center">

| STATE | PURPOSE |
|:---|:---|
| 🟢 NORMAL | System behavior is consistent with the expected operating envelope. |
| 🟡 SUSPECTED FAULT | An inconsistency has been detected and requires evaluation. |
| 🟠 DEGRADED | Operation continues under defined restrictions, if permitted. |
| 🔵 RECOVERY | A recovery or reconfiguration procedure is evaluated. |
| 🔴 SAFE STOP | The system enters a predefined safe condition when required. |

</div>

These states are proposed design elements. Their implementation requires explicit transition conditions, safety constraints, and validation.

---

<!-- ====================================================== -->
<!-- MATLAB / SIMULINK                                      -->
<!-- ====================================================== -->

# ◈ 06 — MATLAB & SIMULINK RESEARCH ENVIRONMENT

The intended implementation environment is MATLAB/Simulink.

Potential development stages include:

- Mathematical modeling of a selected physical plant.
- Baseline controller implementation.
- Reference and measured response comparison.
- Residual calculation and threshold design.
- Fault and disturbance scenario simulation.
- Constrained controller optimization.
- Supervisory mode-transition logic.
- Performance evaluation and result visualization.

### INITIAL TEST PLANT

A DC motor starting system is a potential first test case.

The plant model, controller, disturbance scenarios, and fault conditions should be defined before claiming experimental performance.

---

<!-- ====================================================== -->
<!-- PROJECT METRICS                                        -->
<!-- ====================================================== -->

# ◈ 07 — EVALUATION METRICS

The framework can be evaluated using measurable criteria such as:

| METRIC | EVALUATION PURPOSE |
|:---|:---|
| Detection latency | Time required to detect an inconsistency |
| False alarm rate | Frequency of incorrect fault alarms |
| Diagnosis accuracy | Correctness of fault classification |
| Tracking error | Difference between reference and measured output |
| Control effort | Input required to achieve the control objective |
| Constraint violations | Frequency and severity of limit violations |
| Recovery success | Whether the defined recovery criteria are met |
| Computational cost | Processing time and resource requirements |

**Research integrity:** performance values should be reported only after running the relevant simulations or experiments.

---

<!-- ====================================================== -->
<!-- GETTING STARTED                                        -->
<!-- ====================================================== -->

<a id="getting-started"></a>

# ◈ 08 — GETTING STARTED

### REQUIREMENTS

- MATLAB
- Simulink, if used by the selected implementation
- A defined mathematical model of the chosen plant
- Baseline controller and test scenarios

### PROPOSED WORKFLOW

```text
01  Define the physical plant
          ↓
02  Build and validate its mathematical model
          ↓
03  Implement the baseline controller
          ↓
04  Calculate model-consistency residuals
          ↓
05  Define fault and disturbance scenarios
          ↓
06  Implement diagnosis and supervisory logic
          ↓
07  Evaluate performance and safety constraints
          ↓
08  Document reproducible simulation results
```

---

<!-- ====================================================== -->
<!-- RESEARCH VISION                                        -->
<!-- ====================================================== -->

<div align="center">

<img
  src="https://capsule-render.vercel.app/api?type=rect&height=4&color=0:00E5A8,50:00F0FF,100:755CFF"
  width="100%"
  alt="Research vision divider"
/>

## THE PHYSIOPT-X RESEARCH VISION

### From model-based control to physics-aware verification.

**Predict intelligently. Verify continuously. Optimize responsibly.**

<br/>

![Research](https://img.shields.io/badge/RESEARCH-PHYSICS--AWARE-00F0FF?style=flat-square)
![Control](https://img.shields.io/badge/CONTROL-SELF--VERIFYING-755CFF?style=flat-square)
![Safety](https://img.shields.io/badge/SAFETY-CONSTRAINT--AWARE-00E5A8?style=flat-square)

</div>
```

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=venom&height=300&color=0:080B1A,35:101B3D,70:5427A8,100:00E5FF&text=PHYSIOPT-X&fontColor=FFFFFF&fontSize=75&fontAlignY=43&desc=PHYSICS-AWARE%20INTELLIGENT%20CONTROL&descSize=17&descAlignY=62&animation=fadeIn&stroke=00E5FF&strokeWidth=1" width="100%" alt="PHYSIOPT-X research banner"/>

### ◈ SELF-VERIFYING OPTIMIZATION & FAULT-TOLERANT CONTROL ◈

**Beyond Conventional Control — Toward Physics-Aware Autonomous Systems**

<br>

<img src="https://img.shields.io/badge/DOMAIN-ADVANCED_CONTROL-00E5FF?style=for-the-badge&labelColor=080B1A" alt="Advanced Control"/>
<img src="https://img.shields.io/badge/PLATFORM-MATLAB%20%2F%20SIMULINK-8B5CF6?style=for-the-badge&labelColor=080B1A" alt="MATLAB and Simulink"/>
<img src="https://img.shields.io/badge/RESEARCH-CYBER--PHYSICAL_SYSTEMS-00E5FF?style=for-the-badge&labelColor=080B1A" alt="Cyber-Physical Systems"/>
<img src="https://img.shields.io/badge/FOCUS-FAULT--TOLERANT_AI-B794F6?style=for-the-badge&labelColor=080B1A" alt="Fault-tolerant intelligent control"/>

<br><br>

<table>
<tr>
<td align="center" width="25%">
<h3>◈ 01</h3>
<b>OBSERVE</b><br>
<sub>Physical State Estimation</sub>
</td>
<td align="center" width="25%">
<h3>◈ 02</h3>
<b>VERIFY</b><br>
<sub>Physics Consistency</sub>
</td>
<td align="center" width="25%">
<h3>◈ 03</h3>
<b>OPTIMIZE</b><br>
<sub>Constrained Control</sub>
</td>
<td align="center" width="25%">
<h3>◈ 04</h3>
<b>RECOVER</b><br>
<sub>Supervised Reconfiguration</sub>
</td>
</tr>
</table>

<br>

> **MODEL ≠ REALITY**
>
> When physical behavior diverges from mathematical predictions,  
> the system must detect the discrepancy, investigate its cause,  
> evaluate corrective actions, and verify recovery before accepting it.

<br>

<a href="#-the-research-vision">
<img src="https://img.shields.io/badge/EXPLORE_THE_RESEARCH-00E5FF?style=for-the-badge&labelColor=080B1A" alt="Explore the research"/>
</a>

<a href="#-system-architecture">
<img src="https://img.shields.io/badge/SYSTEM_ARCHITECTURE-8B5CF6?style=for-the-badge&labelColor=080B1A" alt="System architecture"/>
</a>

<a href="#-experimental-framework">
<img src="https://img.shields.io/badge/EXPERIMENTS-00E5FF?style=for-the-badge&labelColor=080B1A" alt="Experiments"/>
</a>

</div>

<img src="https://capsule-render.vercel.app/api?type=rect&height=3&color=0:00E5FF,50:8B5CF6,100:00E5FF" width="100%" alt="Cyan violet divider"/>

## ◈ THE RESEARCH VISION

PHYSIOPT-X is a physics-aware optimization and fault-tolerant control framework designed to investigate how autonomous cyber-physical systems can respond to discrepancies between their mathematical models and actual physical behavior.

<div align="center">

```text
       ┌─────────────────────────────────────────┐
       │           PHYSICAL SYSTEM               │
       │       Sensors · Actuators · Plant       │
       └───────────────────┬─────────────────────┘
                           │
                           ▼
       ┌─────────────────────────────────────────┐
       │       PHYSICS CONSISTENCY ENGINE        │
       │       Prediction  ↔  Measurement        │
       └───────────────────┬─────────────────────┘
                           │
                           ▼
       ┌─────────────────────────────────────────┐
       │        FAULT DETECTION & DIAGNOSIS      │
       │       Residuals · Evidence · Analysis   │
       └───────────────────┬─────────────────────┘
                           │
                           ▼
       ┌─────────────────────────────────────────┐
       │      CONSTRAINED CONTROL OPTIMIZER      │
       │        Candidate Generation             │
       └───────────────────┬─────────────────────┘
                           │
                           ▼
       ┌─────────────────────────────────────────┐
       │       SUPERVISORY VERIFICATION          │
       │       Accept · Degrade · Safe Stop      │
       └───────────────────┬─────────────────────┘
                           │
                           ▼
                  CONTROLLED RESPONSE
```

</div>

<img src="https://capsule-render.vercel.app/api?type=rect&height=2&color=0:8B5CF6,100:00E5FF" width="100%" alt="Section divider"/>

<div align="center">

### ENGINEERED FOR UNCERTAINTY. DESIGNED FOR VERIFICATION.

<sub>MATLAB · Dynamic System Modeling · Fault Diagnosis · Control Optimization · Cyber-Physical Systems</sub>

</div>

PHYSIOPT-X
Physics-Aware Self-Verifying Optimization and Fault-Tolerant Control Framework for Autonomous Cyber-Physical Systems
Research category: Advanced Control Engineering · Model-Based Fault Diagnosis · Adaptive Control · Constrained Optimization · Cyber-Physical Systems

Primary development environment: MATLAB / Simulink

Research level: Advanced Master's thesis, with a clearly defined pathway toward PhD research.

Central research question:
Can an autonomous control framework detect physical inconsistencies, identify plausible system faults, reconfigure a controller under explicit safety constraints, and independently verify the resulting closed-loop behavior before accepting recovery?

PART I — PROJECT FOUNDATION
1. Abstract
PHYSIOPT-X is a proposed physics-aware control and optimization framework for autonomous cyber-physical systems operating under uncertainty, component degradation, sensor faults, actuator limitations, and changing environmental conditions.

Conventional control design often assumes that the mathematical model used during controller synthesis remains sufficiently accurate during operation. In practice, the physical system may gradually or abruptly diverge from its nominal model because of changes in mass, friction, actuator effectiveness, sensor calibration, power availability, or external disturbances.

Such divergence can degrade tracking performance, increase control effort, violate operating constraints, and potentially destabilize the closed-loop system.

PHYSIOPT-X addresses this challenge through an integrated methodology combining physics-based prediction, state estimation, residual generation, fault detection, fault isolation, constrained controller optimization, supervised reconfiguration, and post-reconfiguration verification.

The proposed architecture maintains a distinction between detecting abnormal behavior and establishing its cause. It also distinguishes a controller that performs well in simulation from a controller whose safety properties have been demonstrated under stated assumptions.

The initial implementation targets a nonlinear electromechanical system, such as a DC motor with a variable load, using MATLAB and Simulink. A digital-twin model generates expected behavior, while simulated measurements and injected faults provide a controlled environment for evaluating detection latency, false alarms, diagnosis accuracy, tracking performance, constraint violations, and recovery success.

A constrained optimization layer searches for improved controller parameters. A supervisory safety layer evaluates proposed configurations against predefined operating limits, while a verification layer determines whether the system may return to normal operation, remain in degraded operation, or enter a safe-stop state.

The main research contribution is the integration of physical consistency monitoring, fault-aware optimization, and independently evaluated recovery into a single reproducible experimental framework.

Important research status: This document defines a research proposal and implementation plan. Performance improvements, experimental results, and claims of verified stability must be established by running the implementation and evaluating the resulting evidence; they are not assumed in advance.
2. Introduction
Modern autonomous systems combine physical processes, embedded computation, sensors, actuators, communication networks, and software-based decision-making.

Examples include:
- Autonomous mobile robots.
- Industrial robotic manipulators.
- Electric drives and motor-control systems.
- Autonomous vehicles.
- Smart manufacturing equipment.
- Energy-conversion systems.
- Unmanned aerial vehicles.
- Intelligent industrial automation systems.
These systems must operate despite uncertainties that cannot always be eliminated during design.

A controller may be carefully tuned for a nominal system and perform exceptionally well during initial testing. However, its behavior can deteriorate when the physical plant changes.

For example, a mobile robot may encounter a heavier payload. The additional mass changes its acceleration characteristics. A motor may lose effectiveness because of degradation. A battery may supply a lower voltage. An encoder may produce implausible measurements. Friction may increase because of mechanical wear.

A conventional controller may continue issuing commands without recognizing that the assumptions supporting its design are no longer valid.

PHYSIOPT-X investigates a more resilient alternative: a control architecture that continuously compares expected physical behavior with measured behavior and uses the resulting evidence to guide diagnosis, optimization, and recovery.
2.1 The central engineering principle
The framework begins with a simple observation:
\[
\boxed{\text{Model} \neq \text{Reality}}
\]
This expression represents the possibility of model mismatch, not a claim that the model is always incorrect.

The objective is to quantify the mismatch, determine whether it is consistent with normal uncertainty or a fault, and respond appropriately.
2.2 Research objectives
The project has eight principal objectives.
1. Develop a physics-based model of a selected electromechanical system.
2. Implement state estimation and physical consistency monitoring.
3. Detect deviations caused by defined faults and disturbances.
4. Diagnose faults using residual signatures and multiple evidence sources.
5. Optimize controller parameters under performance and safety constraints.
6. Reconfigure the controller when its existing configuration becomes unsuitable.
7. Evaluate the proposed configuration before accepting recovery.
8. Demonstrate the framework through reproducible MATLAB/Simulink experiments.
2.3 Research hypotheses
The project will test the following hypotheses.

H1 — Fault awareness: Combining physics-based residuals with temporal decision logic can distinguish selected faults from nominal disturbances more reliably than a single instantaneous threshold.

H2 — Fault-aware optimization: Reoptimizing controller parameters after an identified plant change can improve tracking performance compared with retaining the original controller, provided the optimization remains within the feasible operating region.

H3 — Supervised recovery: Separating controller proposals from supervisory acceptance can prevent an unvalidated controller configuration from being applied to the physical plant.

H4 — Graceful degradation: When safe recovery is infeasible, a supervisory controller can direct the system into a predefined degraded mode or safe-stop state.

These hypotheses are testable. None should be described as proven until the corresponding experiments have been completed.
PART II — MATHEMATICAL AND PHYSICAL MODEL
3. Why a DC motor is the right starting point
A doctoral-level framework does not need to begin with an unnecessarily complicated robot. It needs a physical system whose behavior can be modeled, whose faults can be reproduced, and whose control performance can be measured rigorously.

For PHYSIOPT-X, the initial experimental plant will be a permanent-magnet DC motor with electrical and mechanical dynamics.

The motor provides a useful test environment because it has measurable physical parameters, nonlinear operating constraints, controllable disturbances, and fault scenarios that can be introduced independently or simultaneously.

The architecture can later be extended to a mobile robot, robotic manipulator, or other cyber-physical system.
3.1 System state
Define the state vector:






6. Fault detection versus fault diagnosis
These are different tasks.

Fault detection answers:
Has the observed behavior become sufficiently inconsistent with the expected behavior to warrant an alarm?

Fault diagnosis answers:
Which fault or combination of faults best explains the available evidence?

Fault isolation attempts to distinguish the affected component or subsystem.

Fault accommodation modifies the control strategy to tolerate the identified condition.

Fault recovery attempts to restore acceptable operation.

A strong PHYSIOPT-X implementation must not confuse these stages.
6.1 Initial fault library
The first version should include the following reproducible fault scenarios.
Fault ID	Fault	Simulation mechanism	Expected evidence
F00	Nominal operation	No injected fault	Small residuals
F01	Increased load	Increase \(T_L\)	Speed tracking degradation
F02	Increased friction	Increase \(B\)	Increased steady-state torque requirement
F03	Actuator degradation	Reduce \(\eta_a\)	Lower effective motor input
F04	Sensor bias	Add offset to measured speed	Persistent measurement inconsistency
F05	Parameter drift	Gradually change \(J\), \(B\), or \(R\)	Slowly increasing model mismatch
F06	Measurement noise	Increase measurement noise variance	More variable residuals
F07	Actuator saturation	Enforce voltage limits	Control command differs from requested input
F08	Communication delay	Delay measurements or commands	Phase lag and prediction error
F09	Multiple faults	Combine selected faults	Overlapping residual signatures


The table describes proposed experiments, not results that have already been obtained.
6.2 Fault signatures
For a more advanced diagnosis system, each fault can be associated with a vector of features:
\[
\phi_k=
\begin{bmatrix}
r_{\omega,k}\\
r_{i,k}\\
\Delta y_k\\
u_k\\
\hat{J}_k\\
\hat{B}_k\\
\hat{\eta}_{a,k}
\end{bmatrix}
\]
Here, the residuals, estimated parameters, and control signals provide complementary evidence.

For example:
- A load increase may affect mechanical acceleration while leaving the electrical circuit parameters unchanged.
- A resistance increase may affect the current response and electrical time constant.
- A sensor bias may produce disagreement between the measurement and a model prediction even when the underlying plant is healthy.
- Actuator degradation may produce lower physical response for a given requested input.
These signatures are not universally unique. Two faults may be observationally indistinguishable under a particular experiment.

Consequently, diagnosis accuracy depends on the available sensors, excitation signals, operating conditions, model quality, and fault definitions.
6.3 Advanced diagnosis options
After the initial residual detector works, the framework can be extended using:
1. Moving-window statistical tests.
2. Cumulative-sum detection.
3. Generalized likelihood-ratio methods.
4. Model-based fault isolation.
5. Recursive parameter estimation.
6. Bayesian fault classification.
7. Supervised machine-learning classifiers trained on simulated fault signatures.
8. Unknown-fault detection based on out-of-distribution behavior.
Machine learning should not replace the physics model without a reason. Its role is to complement model-based diagnosis where multiple faults generate similar residual patterns.
PART IV — CONTROL AND OPTIMIZATION
7. Baseline controller: PID
The proportional-integral-derivative controller provides the baseline against which more advanced methods can be compared.

Define the tracking error:
\[
e(t)=\omega_{\mathrm{ref}}(t)-\omega(t)
\]
The ideal PID law is:
\[
u(t)=K_pe(t)
+K_i\int_0^t e(\tau)\,d\tau
+K_d\frac{de(t)}{dt}
\]
where:
- \(K_p\) controls proportional response.
- \(K_i\) compensates for persistent tracking error.
- \(K_d\) responds to error-rate changes.
The implemented control command must respect the motor's voltage limits:
\[
u_{\mathrm{applied}}
=
\operatorname{sat}
\left(
u_{\mathrm{requested}},
-V_{\max},V_{\max}
\right)
\]
This distinction matters because the requested voltage and the applied voltage are not necessarily identical.
7.1 Integral windup
When the actuator saturates, the integral term can continue accumulating error even though the actuator cannot supply the requested input.

This is called integral windup.

The implementation should therefore include an anti-windup mechanism, such as conditional integration or back-calculation.

The first executable prototype below uses a conditional-integration approach. A production-quality implementation should additionally evaluate derivative filtering, bumpless transfer, and recovery from prolonged saturation.

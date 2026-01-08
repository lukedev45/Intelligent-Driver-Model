# Intelligent Driver Model

A Jupyter-Notebook implementation of the **Intelligent Driver Model (IDM)** — a classical *microscopic car-following traffic model* for simulating vehicle longitudinal dynamics in traffic flow. IDM computes vehicle acceleration based on the current speed, desired speed, gap to the vehicle ahead, and relative speed, producing realistic acceleration and braking behaviour in simulated traffic. :contentReference[oaicite:0]{index=0}

This repository includes:
- A complete notebook modelling IDM from first principles
- A written PDF report documenting the theory, implementation, and results

## 🚗 What is the Intelligent Driver Model?

The Intelligent Driver Model is a **time-continuous car-following model** that describes how a vehicle reacts dynamically to the vehicle in front of it — balancing desire for speed with safe following distance. IDM has become a foundational model in traffic flow simulation due to its simplicity and ability to capture realistic traffic dynamics. :contentReference[oaicite:1]{index=1}

It uses inputs including:
- **own vehicle speed**
- **gap to the leading vehicle**
- **relative speed**

to compute a smooth acceleration/deceleration profile. IDM can produce realistic behaviours like approaching safe headways and adjusting to traffic slowdowns without unrealistic oscillations. :contentReference[oaicite:2]{index=2}

## 🧠 Background & Theory

IDM is mathematically defined by:

dv/dt = a · [ 1 − (v / v₀)^δ − (s*(v, Δv) / s)² ]

where:
- `v` is current speed
- `v0` is desired speed
- `s` is gap to the car ahead
- `Δv` is speed difference to the vehicle ahead  
- `s*(v, Δv)` is the desired dynamic spacing

These inputs and the model structure ensure smooth, collision-free dynamics that respect driver comfort and safe following rules. :contentReference[oaicite:3]{index=3}

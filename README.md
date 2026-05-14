# Brain-Controlled Wheelchair — BCI Assistive Mobility System

A Brain-Computer Interface (BCI) controlled wheelchair designed to enable mobility-impaired individuals to navigate independently using motor imagery — imagined movements of hands, feet, and tongue translated into wheelchair commands via EEG signal classification.

![Wheelchair Assembly Drawing](images/assembly_drawing.jpg)

## Overview

This project was developed as part of the **Advanced Mechatronics System Design**(Feb–Jul 2024). This project was collaborated to design a complete system spanning EEG signal acquisition, deep learning classification, embedded motor control, and mechanical wheelchair design.

My role focused on the **CAD design and structural modelling** of the wheelchair using Fusion 360.

## How It Works

```
  ┌────────────────┐
  │   EEG Headset   │   User imagines moving left hand,
  │ (Ultracortex    │   right hand, feet, or tongue
  │  Mark IV, 8ch)  │
  └───────┬────────┘
          │ Neural signals
          ▼
  ┌────────────────┐
  │ Signal          │   Bandpass filter (8-30 Hz)
  │ Processing      │   Artifact removal (ICA)
  │ (MATLAB)        │   Feature extraction
  └───────┬────────┘
          │ Cleaned EEG data
          ▼
  ┌────────────────┐
  │ Classification  │   CNN / SVM / VAE
  │ (Deep Learning) │   4-class: left, right, forward, stop
  └───────┬────────┘
          │ Command label (1-4)
          ▼
  ┌────────────────┐
  │ Embedded System │   ATmega8 microcontroller
  │ (Bluetooth)     │   Motor drivers + relay control
  └───────┬────────┘
          │ Motor signals
          ▼
  ┌────────────────┐
  │  Wheelchair     │   2× DC motors (powered wheels)
  │  (Mechanical)   │   2× casters (front)
  └────────────────┘
```

## My Contribution — Wheelchair CAD Design

I was responsible for the complete mechanical design of the wheelchair using **Fusion 360**, including:

- **2D technical sketches** with dimensioned side, front, back, and top views
- **3D CAD modelling** of the full wheelchair assembly
- **Component design** — backrest, armrests, footrest, motor housing, powered wheel mounts, caster assemblies, and laptop mount
- **Material selection** — lightweight metals (aluminium, titanium) for the frame, high-density foam for seating, polycarbonate/CFRP for the footrest, reinforced rubber for tyres
- **Ergonomic design** — ensuring comfort, manoeuvrability, and structural integrity for the end user
- **Engineering drawings** — assembly drawing with parts list, dimensioning, and orthographic views

### Key Design Dimensions

| Parameter | Value |
|-----------|-------|
| Wheel diameter | 304.8 mm (12 in) |
| Caster diameter | 130 mm |
| Seat width | 350 mm |
| Seat depth | 347 mm |
| Backrest height | 350 mm |
| Armrest width | 260 mm |
| Motor housing height | 146.84 mm |
| Overall frame height | 569.68 mm |

## System Components

| Subsystem | Component | Purpose |
|-----------|-----------|---------|
| Data Acquisition | Ultracortex Mark IV (8-channel EEG) | Captures motor imagery brain signals |
| Signal Processing | MATLAB pipeline | Filtering, artifact removal, feature extraction |
| Classification | CNN / SVM / VAE | Classifies EEG into 4 movement commands |
| Embedded Control | ATmega8 + HC-05 Bluetooth | Receives commands, drives motors |
| Motor Drive | Sabertooth 2×32 dual driver | Controls 2× DC wheelchair motors |
| Power | TalentCell 24V Li-ion battery | Powers motors and electronics |
| Structure | Custom Fusion 360 wheelchair design | Ergonomic, lightweight, manoeuvrable frame |

## Context

Developed for the **Advanced Mechatronics System Design**. The project bridges robotics, biomedical engineering, embedded systems, and mechanical design into a single multidisciplinary assistive technology solution.

## Skills Demonstrated

- CAD modelling and mechanical design (Fusion 360)
- Engineering drawing creation (orthographic views, dimensioning, parts lists)
- Material selection for assistive devices
- Ergonomic design principles
- Multidisciplinary team collaboration (robotics × biomedical × embedded)
- Technical presentation to academic and cross-disciplinary audiences

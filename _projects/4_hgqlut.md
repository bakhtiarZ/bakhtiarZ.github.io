---
layout: page
title: HGQ-LUT
description: A collaborative FPGA inference project combining LUT-aware training, heterogeneous quantization, and end-to-end hardware generation for hybrid neural networks.
importance: 3
category: phd
---

HGQ-LUT is a collaborative research project on fast LUT-aware training and deployable FPGA architectures for deep neural network inference. I contributed to the work as part of a broader co-authored effort; this is not a solo project. The paper was accepted at FCCM 2026.

At a high level, the work makes LUT-based neural inference much more practical by combining efficient training with hardware-aware quantization and an end-to-end deployment flow. The framework introduces LUT-Dense and LUT-Conv layers that can be trained efficiently with standard tensor operations, then compiled into FPGA logic for low-latency inference.

The project also integrates with the HGQ and da4ml toolchains so LUT-based and conventional arithmetic layers can be used in the same model, compiled through a unified workflow, and verified bit-exactly before RTL deployment. This matters because it lowers the barrier to building hybrid architectures instead of forcing an all-or-nothing LUT-based design.

The resulting framework improves the training cost of LUT-aware methods substantially while preserving strong hardware efficiency, making low-latency LUT-based inference more realistic for real deployment settings such as high-energy physics systems.

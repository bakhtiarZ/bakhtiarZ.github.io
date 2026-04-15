---
layout: page
title: ARRC
description: A research compiler that lowers quantized Keras models into a streaming IR and emits FPGA-oriented SystemVerilog.
importance: 2
category: phd
---

ARRC is a research hardware-compilation project for turning quantized neural networks into synthesizable streaming RTL. The goal is to bridge high-level HGQ and da4ml style models with practical FPGA-oriented hardware generation by lowering Keras-based quantized networks into an intermediate representation that captures dataflow, streaming shapes, routing, and bitwidth contracts.

The project focuses on preserving the structure of the original network while making it hardware-aware. It supports lowering dense layers, reductions such as `QSum`, and streamed 1D convolutions, while reasoning about parallelism, buffering, shift-register windows, and fixed-point interfaces between nodes.

A major part of the work is quantization handling. The compiler replays HGQ symbolic semantics, derives tensor bitwidths, validates inter-layer compatibility, and surfaces cases where explicit hardware adapters would be needed. On the backend side, the system emits SystemVerilog for top-level modules, buffers, and custom datapaths, with end-to-end validation using cocotb, Verilator, and synthesis-oriented tooling.

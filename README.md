# Minimizing Energy Consumption in Computer Networks via Convex Optimization

This repository contains the code and documentation for the project titled **"Minimizing Energy Consumption in Computer Networks via Convex Optimization"** by **Mohammad Raihan Uddin**.

## Table of Contents

- [Introduction](#introduction)
- [System Model and Problem Formulation](#system-model-and-problem-formulation)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Simulation Results](#simulation-results)
- [Project Structure](#project-structure)
- [License](#license)
- [Contact Information](#contact-information)

## Introduction

Energy efficiency is a critical aspect of modern computer networks. This project presents a convex optimization approach to minimize energy consumption in computer networks by jointly optimizing CPU frequency and transmit power under constraints. Frequency Division Multiple Access (FDMA) is used as the transmission protocol. The objective is to explore the trade-offs between energy consumption, system performance, and operational constraints through various simulation scenarios.

## System Model and Problem Formulation

The system model involves multiple user devices (UDs) that execute tasks locally and offload data to a base station (BS). The problem is formulated as a convex optimization problem with the goal of minimizing the total energy consumption while satisfying latency and power constraints. The optimization variables are CPU frequency and transmit power.

For detailed mathematical formulations, please refer to the `paper.pdf` included in this repository.

## Requirements

- **MATLAB** (R2018b or later recommended)
- **YALMIP** toolbox ([Download YALMIP](https://yalmip.github.io/download/))
- **Optimization Solver** compatible with YALMIP (e.g., `fmincon`, `sdpt3`, `sedumi`)
- **LaTeX** distribution (e.g., TeX Live, MikTeX) for compiling the paper

## Installation

1. **Clone the Repository**

   ```bash
   git clone https://github.com/yourusername/your-repo-name.git

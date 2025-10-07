# LLM-FEA-Optimization

**Intelligent Coordination of Data-Driven and Physics-Based Models for Automatic Design of Ultra-High-Performance Concrete Beams**

[![Paper](https://img.shields.io/badge/Paper-Under%20Review-blue)]()
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

## Overview

This repository contains supplementary materials for our research on LLM-integrated structural optimization. The framework coordinates Large Language Models with genetic algorithms (NSGA-II) and Finite Element Analysis (FEA) to automate the design optimization of structural components through natural language interaction.

### Key Innovations

- 🗣️ **Natural Language Interface**: Engineers formulate complex optimization tasks through conversational queries without specialized expertise
- 🧠 **Adaptive Parameter Refinement**: LLM agents automatically adjust optimization parameters based on performance feedback, reducing computational time by 76%
- ⚙️ **Physics-Based Validation**: Seamless integration with ABAQUS FEA ensures reliable, code-compliant solutions
- 📊 **Multi-Objective Optimization**: Generates Pareto-optimal solutions exploring cost-performance trade-offs
- 🤝 **Interactive Decision Support**: Conversational interface for exploring design alternatives and verifying safety requirements

### Performance Highlights

- **88% reduction** in human effort vs. manual design
- **76% reduction** in computational time vs. traditional optimization (50×50 parameters)
- **Perfect accuracy** (F1-score = 1.0) on 30 diverse test queries
- **5.2 hours** total time to generate 27 Pareto-optimal solutions

## Framework Architecture

The system comprises three integrated modules:

### 1. Planning Module
Parses natural language queries and determines optimization parameters using agentic Retrieval-Augmented Generation (RAG):
- Query processor extracts design requirements
- Agentic RAG retrieves relevant design codes and research findings
- Parameter initialization for NSGA-II and FEA setup

### 2. Implementing Module
Executes structural optimization with physics-based evaluation:
- NSGA-II multi-objective genetic algorithm
- Automated ABAQUS FEA model generation and analysis
- Refinement agent monitors performance and adjusts parameters

### 3. Evaluating Module
Provides conversational analysis and verification:
- Interactive exploration of Pareto front solutions
- ACI 318-25 code compliance verification
- Multi-modal interface (text + images) for design discussion

## Repository Contents

### 📖 Documentation
- **[GUI Demonstration](gui_demonstration/)** - Screenshots and usage examples of the graphical interface
- **[Test Queries](test_queries.txt)** - 30 validation queries spanning diverse design scenarios used to evaluate system reliability (Precision/Recall/F1 = 1.0)

### 🎬 Demonstration
- **[Animation](gui_demonstration/images/Animation.gif)** - Interactive workflow demonstration

### 💻 Source Code
**Status**: Under development. Source code will be released upon publication and code maturation.

The full implementation will include:
- LLM agent orchestration (LangChain-based)
- Python-ABAQUS FEA integration scripts
- NSGA-II optimization pipeline with adaptive refinement
- Parameterized UHPC beam model templates
- Streamlit-based GUI implementation
- Agentic RAG system with vector database

**Early Access**: Researchers interested in collaboration or early access may contact the corresponding author.

## Technology Stack

- **LLM**: Gemini 2.5 Flash (gemini-2.5-flash-preview-05-20)
- **Optimization**: NSGA-II (Non-dominated Sorting Genetic Algorithm II)
- **FEA**: ABAQUS with Concrete Damage Plasticity (CDP) model
- **Framework**: LangChain for agent orchestration
- **Interface**: Streamlit for GUI
- **RAG**: Vector database with hybrid search (semantic + BM25)

## Case Study: UHPC Beam Optimization

The framework is demonstrated through Ultra-High Performance Concrete (UHPC) beam design, where:
- Underdeveloped design codes necessitate FEA-based evaluation
- Superior material properties enable unconventional designs (e.g., minimal/no stirrups)
- Multi-objective optimization explores

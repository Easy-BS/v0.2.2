# Easy-BS v0.2.2
🔔Easy-BS (Easy-Building-Simulation) is an AI-agent–driven building performance simulation framework that enables non-expert users to generate, modify, and simulate building energy models using natural language.
=======================
🆕 What's New in v0.2.2
Natural-language multi-zone layout, without coordinates

In v0.0.1, irregular multi-zone plans required the user to type explicit room polygon coordinates. This version removes that requirement.

Plans are now described relationally, using room dimensions and ordinary spatial statements:

Room_1 is 3.5 m wide and 3.7 m deep, in the southwest corner.
The Closet is 2.3 m wide and 1.0 m deep, directly north of Room_1,
with their west walls flush.

A new topology-to-geometry constraint solver (Multi_flow/nodes/layout_solver.py) resolves these statements into absolute room polygons by exact integer propagation over a room adjacency graph. Five relation types are supported: corner, adjacent, align, offset, and center.

The description is much shorter than the geometry it specifies. For the largest test plan, 18 stated relations position 12 rooms whose resolved layout contains 23 inter-zone contacts. The user describes the arrangement; the topology is derived.

All four multi-zone test plans resolve to layouts identical to their reference coordinates, verified by exact vertex match.

Explicit coordinate input remains supported as an alternative mode, so existing scripts continue to work.

=======================
This project explores how Large Language Models (LLMs) and AI-Agent systems can automate traditionally expert-driven building simulation workflows such as:

• Geometry creation

• Simulation setup 

• Result interpretation
<p align="center">
  <img src="docs/Picture1_.svg" width="700">
</p>

🚀 Key Features

✅ Natural-language-driven building model generation

✅ A modular LLM-driven multi-agent simulation framework

✅ Integration with EnergyPlus simulation engine

✅ Automated error correction and workflow validation

✅ Designed for early-stage design and non-expert users

🏗️ System Architecture

The Easy-BS (Easy-Building-Simulation) framework consists of AI agents that collaborate to construct and simulate building models through structured reasoning and tool execution.

<p align="center">
  <img src="docs/Picture4.svg" width="700">
</p>

📁 Project Structure

Folder	Description

easybs/	Core agent framework

examples/	Sample building simulation cases

docs/	Architecture diagrams and figures


📊 Demonstration

<p align="center">
  <img src="docs/Demo_1.0.1.gif" width="700">
</p>

⚠️ Project Status

This project is under active academic development. Interfaces may change as research progresses.

📄 Related Paper

(TBD)

📚 Citation

(TBD)

📜 License

MIT License



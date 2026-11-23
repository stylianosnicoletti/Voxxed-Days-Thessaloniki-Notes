# Voxxed Days Thessaloniki – Notes

## Day 1

### 1. Identifying and Fixing Issues in Code Using AI-Based Tools

- Treat AI as a tool, not a source of truth. Always validate its suggestions.
- <mark>Use AI to understand complex, unfamiliar, or difficult-to-understand code.</mark>
- Identify code smells, bugs, and potential improvements.

### 2. Our Path to an Agentic Design System

- <mark>Design tokens for consistent theming, colours, typography, and spacing.</mark>
- AI agents can help maintain and evolve centralized design systems.
- Improve consistency and reduce duplicated work across teams.

### 3. Making Clusters Predictable: AI-Powered Kubernetes Diagnostics Using MCP

- OpenCode and Forge MCP connect AI agents to Kubernetes pods.
- <mark>The MCP server exposes controlled tools based on user groups and permissions.</mark>
- <mark>Advertise only authorized tools to agents.</mark>
- Generate HTML reports with pod information and cluster diagnostics.

### 4. Tour of Agent Protocols: MCP, A2A, AG-UI, A2UI

- **MCP:** Connect AI agents to external tools and services.
- **A2A:** Communication between independent agents.
- **AG-UI / A2UI:** Agent-to-UI interaction and rendering.
- <mark>**UCP:** Universal Commerce Protocol for checkout (new).</mark>
- <mark>**AP2:** Agent Payments Protocol (new).</mark>
- <mark>MCP Inspector for testing MCP servers before deployment.</mark>
- <mark>A2A Agent Cards advertise agent capabilities (over a `.well-known` endpoint).</mark>
- A2A SDKs and implementations are available across different languages.

**Presentation slides:** [genai-beyond-basics](https://github.com/meteatamel/genai-beyond-basics)

### 5. The Lazy Engineer's Guide to Scaling

- Automate repetitive tasks and daily checks.
- <mark>Make systems configurable rather than hardcoding values.</mark>
- Reduce manual intervention through automation.

### 6. Has AI Broken Security?

- Increasingly sophisticated exploits and insider threats.
- <mark>Keep dependencies and software versions updated.</mark>
- Prioritize upgrading legacy systems.
- <mark>"Inside jobs 99.9% of time > exploit sophisticated vulnerabilities"</mark>

### 7. The Last Pull Request

- <mark>Experimentation is essential for innovation.</mark>
- <mark>Complex problems require trying different approaches.</mark>
- Validate assumptions before committing to a solution.

### 8. Turning a Distributed Enterprise System into AI Infrastructure

- <mark>Existing workflows are essentially agents under a different name.</mark>
- <mark>MCP Gateway as a centralized entry point for multiple MCP servers.</mark>
- Dynamic registration and refreshing of MCP servers and tools.
- WebSockets and Server-Sent Events (SSE) for communication.
- <mark>Minimize token consumption by exposing only relevant tools.</mark>
- <mark>Use search/filtering and authorization to control tool discovery.</mark>
- <mark>Handle long-running operations asynchronously (new way) or by polling.</mark>
- <mark>Subagents behind MCP tools vs. independent agents communicating through A2A.</mark>

## Day 2

### 1. Building Scalable Multi-Agentic AI Systems with Event-Driven Approach

- Event-driven architecture for communication between agents.
- <mark>Decouple agents to improve scalability and maintainability.</mark>
- <mark>Support asynchronous workflows and long-running operations.</mark>

**Presentation video**

### 2. Has AI Broken Application Security Forever?

- Black-market vulnerability prices: approximately $15K on average, potentially reaching $1.5M.
- <mark>CVEs reportedly doubled over the previous eight months.</mark>
- <mark>AI-generated code can introduce vulnerabilities through outdated dependencies (libraries).</mark>
- **Syft:** Generates SBOMs.
- **Grype:** Scans for known vulnerabilities.
- **Trivy:** Scans images, dependencies, and configurations.
- <mark>Understand where scanners obtain their vulnerability data (outdated public/private datasets).</mark>
- <mark>NVD scoring coverage is incomplete. Don't rely exclusively on scanner scores.</mark>
- Finding vulnerabilities is becoming cheap; fixing them requires engineering effort.
- <mark>Approximately 1 in 8 reported vulnerabilities had an available fix (as mentioned in the talk).</mark>
- HeroDevs provides support for certain end-of-life dependencies.
- <mark>AI-generated security patches must be validated; they may not fix the actual root cause.</mark>

### 3. Machines, Learning, and Machine Learning

- <mark>Vibe coding can result in developers losing understanding of their code over time.</mark>
- Maintain ownership and understanding of AI-generated solutions.
- LM Studio for running local LLMs.
- <mark>Invest in hardware; consider on-premises for more control, privacy, and predictable model versions.</mark>

### 4. How Not to Get Hacked

- <mark>Insider threats are a significant security risk (99.9% of the times).</mark>
- <mark>Absolute Zero Trust: never assume users or systems should automatically be trusted.</mark>
- <mark>Nobody should have unrestricted access to all records, including the CEO.</mark>
- <mark>Apply least privilege and separate systems and permissions.</mark>
- Protect Active Directory and sensitive files such as `NTDS.dit`.
- Tokenize sensitive information.
- <mark>Use one-time nonces (tokenization) on requests (3DS example): layer A calling layer B, layer B calling layer C, but layer A cannot directly call layer C.</mark>

### 5. The AI We Should Build: "Algor-Ethics", Local Models, and Human Dignity

- Use statistical representation of how much damage it is doing to the environment on every search you do on ChatGPT, etc.

### 6. Q-day is coming! Cryptography in a post-quantum world

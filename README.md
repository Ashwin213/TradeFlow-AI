TradeFlow AI

An automated market analysis tool built with Google's Agent Development Kit (ADK) and Gemini 2.0 Flash.

Author: [Ashwin213]
Focus: NAS100 & US30 (New York Session)

Why I Built This
As a day trader, I found myself overwhelmed trying to analyze technicals, check news sentiment, and calculate risk across multiple monitors during the volatility of the New York Open.

I created TradeFlow to offload the repetitive parts of my trading routine. Instead of manually checking RSI/MACD and reading Bloomberg headlines, I built a multi-agent system to do it for me in seconds.

System Architecture
The project uses a Hub-and-Spoke pattern. A central coordinator (Gemini 2.0) takes my natural language queries and delegates them to specialized Python agents.

```mermaid
graph TD
    User --> Coordinator[Coordinator (Gemini 2.0)]
    Coordinator --> Monitor[Market Monitor (Parallel)]
    Coordinator --> News[News Sentinel (LLM)]
    Coordinator --> Risk[Risk Manager (Sequential)]
    Coordinator --> Signal[Signal Generator (Loop)]

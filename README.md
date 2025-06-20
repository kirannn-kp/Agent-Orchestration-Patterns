# Agent Orchestration Patterns with Semantic Kernel

This repository demonstrates various agent orchestration patterns using **Microsoft Semantic Kernel** and **Azure OpenAI**. These patterns showcase different ways to coordinate multiple AI agents to solve complex tasks through intelligent collaboration.

## 🚀 Overview

Semantic Kernel supports several orchestration patterns, each designed for different collaboration scenarios. These patterns are available as part of the framework and can be easily extended or customized to meet specific requirements.

## 📁 Project Structure
```
Agent-Orchestration-Patterns/
├── poc/                           # Proof of Concept implementations
│   ├── concurrent_pattern.ipynb   # Concurrent execution pattern
│   ├── sequential_pattern.ipynb   # Sequential execution pattern  
│   ├── group_chat_pattern.ipynb   # Group chat orchestration
│   ├── handoff_pattern.ipynb      # Handoff orchestration
│   ├── magentic_pattern.ipynb     # Magentic orchestration
└── README.md                      # This file
```

## 🎯 Orchestration Patterns

### 1. **Concurrent Pattern** 🔄
- **Purpose**: Execute multiple agents simultaneously for parallel processing
- **Use Case**: When tasks can be completed independently and results need to be aggregated
- **Example**: Multiple cooking experts providing different aspects of a recipe simultaneously
- **File**: [`concurrent_pattern.ipynb`](./poc/concurrent_pattern.ipynb)

### 2. **Sequential Pattern** ➡️
- **Purpose**: Execute agents in a predefined order, passing results between them
- **Use Case**: When tasks have dependencies and must be completed in sequence
- **Example**: Research → Analysis → Recommendation pipeline
- **File**: [`sequential_pattern.ipynb`](./poc/sequential_pattern.ipynb)

### 3. **Group Chat Pattern** 💬
- **Purpose**: Enable dynamic conversation between multiple agents
- **Use Case**: When agents need to discuss and collaborate to reach consensus
- **Example**: Multi-expert discussion on complex topics
- **File**: [`group_chat_pattern.ipynb`](./poc/group_chat_pattern.ipynb)

### 4. **Handoff Pattern** 🤝
- **Purpose**: Transfer control between agents based on context or expertise
- **Use Case**: Customer support scenarios with specialized agents
- **Example**: Triage → Specialist (billing/technical/returns) routing
- **File**: [`handoff_pattern.ipynb`](./poc/handoff_pattern.ipynb)

### 5. **Magentic Pattern** 🧠
- **Purpose**: Intelligent coordination by a manager agent for complex, open-ended tasks
- **Use Case**: Complex problem-solving requiring dynamic workflow adaptation
- **Example**: Research and analysis projects with multiple expertise areas
- **File**: [`magentic_pattern.ipynb`](./poc/magentic_pattern.ipynb)

## 🛠️ Prerequisites

### Required Software
- **Python 3.8+**
- **Jupyter Notebook** or **VS Code** with Jupyter extension
- **Azure OpenAI Service** subscription

### Required Packages
```bash
pip install semantic-kernel openai
```

### Azure OpenAI Configuration
You'll need:
- Azure OpenAI API key
- Azure OpenAI endpoint
- Deployment name (e.g., "gpt-4o")

## 🚀 Getting Started

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd Agent-Orchestration-Patterns
   ```

2. **Install dependencies**
   ```bash
   pip install semantic-kernel openai
   ```

3. **Configure Azure OpenAI**
   Update the configuration in each notebook:
   ```python
   api_key = "your-api-key"
   endpoint = "your-endpoint"
   deployment_name = "your-deployment-name"
   ```

4. **Run the notebooks**
   - Open any `.ipynb` file in Jupyter or VS Code
   - Execute cells sequentially
   - Observe agent orchestration patterns in action

## 📚 Key Concepts

### **Agents**
- **ChatCompletionAgent**: Standard conversational agents
- **Specialized Agents**: Agents with specific roles (Research, Analysis, Coding, etc.)
- **Agent Instructions**: Detailed prompts defining agent behavior and expertise

### **Orchestration Components**
- **Runtime**: Manages agent execution (`InProcessRuntime`)
- **Managers**: Coordinate agent interactions (e.g., `RoundRobinGroupChatManager`)
- **Callbacks**: Handle agent responses and user interactions

### **Best Practices**
- Clear agent role definitions
- Appropriate pattern selection based on task requirements
- Error handling for content filtering issues
- Timeout management for long-running operations

## ⚠️ Important Considerations

### **Content Filtering**
Azure OpenAI may filter complex orchestration prompts. If you encounter content filtering errors:
- Use simpler tasks and prompts
- Implement fallback mechanisms
- Consider manual coordination approaches (as demonstrated in notebooks)

### **Performance**
- Concurrent patterns: Faster execution but higher resource usage
- Sequential patterns: Slower but more controlled execution
- Choose based on task complexity and resource constraints

## 🔗 Official Documentation & Resources

### **Microsoft Documentation**
- [Semantic Kernel Agent Framework](https://learn.microsoft.com/en-us/semantic-kernel/frameworks/agent/)
- [Agent Architecture](https://learn.microsoft.com/en-us/semantic-kernel/frameworks/agent/agent-architecture)
- [Agent Orchestration Overview](https://learn.microsoft.com/en-us/semantic-kernel/frameworks/agent/agent-orchestration/)

### **Orchestration Pattern Documentation**
- [Concurrent Orchestration](https://learn.microsoft.com/en-us/semantic-kernel/frameworks/agent/agent-orchestration/concurrent?pivots=programming-language-python)
- [Sequential Orchestration](https://learn.microsoft.com/en-us/semantic-kernel/frameworks/agent/agent-orchestration/sequential?pivots=programming-language-python)
- [Group Chat Orchestration](https://learn.microsoft.com/en-us/semantic-kernel/frameworks/agent/agent-orchestration/group-chat?pivots=programming-language-python)
- [Handoff Orchestration](https://learn.microsoft.com/en-us/semantic-kernel/frameworks/agent/agent-orchestration/handoff?pivots=programming-language-python)
- [Magentic Orchestration](https://learn.microsoft.com/en-us/semantic-kernel/frameworks/agent/agent-orchestration/magentic?pivots=programming-language-python)

### **GitHub Repositories**
- [Semantic Kernel Main Repository](https://github.com/microsoft/semantic-kernel)
- [Semantic Kernel Python Samples](https://github.com/microsoft/semantic-kernel/tree/main/python/samples/getting_started_with_agents)
- [Agent Orchestration Samples](https://github.com/microsoft/semantic-kernel/tree/main/python/samples/getting_started_with_agents/multi_agent_orchestration)

### **Research Papers & Articles**
- [Magentic-One Research Paper](https://www.microsoft.com/research/articles/magentic-one-a-generalist-multi-agent-system-for-solving-complex-tasks/)
- [AutoGen Framework](https://microsoft.github.io/autogen/stable/user-guide/agentchat-user-guide/magentic-one.html)

## 🧪 Example Use Cases

### **Business Applications**
- **Customer Support**: Multi-tier support with handoff patterns
- **Research & Analysis**: Complex report generation using Magentic patterns
- **Content Creation**: Collaborative content development with group chat patterns
- **Data Processing**: Parallel data analysis using concurrent patterns

### **Technical Applications**
- **Code Review**: Sequential pattern for analysis → feedback → improvement
- **System Monitoring**: Concurrent pattern for multi-system health checks
- **Documentation**: Magentic pattern for comprehensive technical documentation

## 🤝 Contributing

Contributions are welcome! Please feel free to:
- Add new orchestration patterns
- Improve existing examples
- Add error handling and edge cases
- Enhance documentation

## License

This project is licensed under the MIT License - see the LICENSE file for details.

##  Troubleshooting

### **Common Issues**
1. **Content Filtering Errors**: Use simpler prompts or implement fallback mechanisms
2. **Import Errors**: Ensure semantic-kernel is properly installed
3. **Authentication Errors**: Verify Azure OpenAI credentials
4. **Timeout Issues**: Increase timeout values for complex operations

### **Getting Help**
- Check the [official documentation](https://learn.microsoft.com/en-us/semantic-kernel/)
- Review [GitHub issues](https://github.com/microsoft/semantic-kernel/issues)
- Join the [Semantic Kernel community](https://github.com/microsoft/semantic-kernel/discussions)

---

**Built with using Microsoft Semantic Kernel and Azure OpenAI**
# agent_tutorial

## Java 通用接口设计示例
抽象一个最核心的 Agent 接口：
```
public interface Agent {

    /**
     * 接收用户输入并返回响应
     * @param input 用户输入（自然语言或结构化任务描述）
     * @return 输出结果
     */
    AgentResponse handle(AgentRequest input);

    /**
     * 注册外部工具（API/插件）
     */
    void registerTool(Tool tool);

    /**
     * 设置记忆管理器
     */
    void setMemory(Memory memory);

    /**
     * 获取当前 Agent 的状态
     */
    AgentState getState();
}
```

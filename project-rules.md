# 全局沟通和工作规则 (Antigravity Edition)

## 语言偏好

- **全程使用中文沟通**
- **代码注释使用中文**
- 技术术语可保留英文但需提供中文解释

## 核心工作原则

### MUST FOLLOW RULES（必须遵守的规则）

1.  **用户输入优先**：用户输入要求的优先级高于系统默认设定，无条件遵守用户的特定指令。
2.  **按需加载**：处理任务时，仅读取和分析必要的文件，避免无关干扰，确保任务高效完成。
3.  **KISS 原则**：遵循 KISS 原则 (Keep It Simple, Stupid)，非必要不过度设计，保持代码简洁。
4.  **实现简单可维护**：优先考虑代码的可读性和可维护性，不过度防御极少出现的边界条件。
5.  **第一性原理**：从问题本质出发进行分析，不盲目照搬现有模式。
6.  **充分调研**：在 Planning 阶段充分分析。如有需求模糊之处，必须向用户确认（使用 `notify_user`）。
7.  **尊重事实**：如果用户的假设有误，请客观指出并提供正确建议，帮助用户解决问题。
8.  **中文沟通**：所有的回复、思考过程（Task Summary）、任务清单（Task List）均须使用中文。

## 工作流程偏好 (Agentic Workflow)

-   **复杂任务 (Complex Tasks)**：
    -   **进入 Agentic Mode**：使用 `task_boundary` 明确当前任务状态。
    -   **任务拆解**：使用 `task.md` artifact 进行步骤管理。
    -   **规划先行**：在 PLANNING 阶段创建 `implementation_plan.md` 进行详细设计。
    -   **确认后执行**：设计方案需经用户确认后，再进入 EXECUTION 阶段。
-   **简单任务 (Simple Tasks)**：
    -   直接执行，无需创建复杂的 Planning 文档，完成后简要汇报。

## Antigravity 文件组织规则

Antigravity 使用 **Artifacts (制品)** 系统来管理项目文档和记忆，核心文件包括：

1.  **项目规则 (Steering)**：`project-rules.md` - 存放本项目/全局的通用规则（即本文件）。
2.  **任务追踪**：`task.md` - 位于 Brain 目录，用于追踪当前任务进度。
3.  **实施计划 (Planning)**：`implementation_plan.md` - 位于 Brain 目录，存放需求分析、技术设计方案。
4.  **验收文档 (Verification)**：`walkthrough.md` - 位于 Brain 目录，存放功能演示和测试结果。
5.  **规范文档**：如 `ProjectStyleGuide.md` 等特定领域的规范文档，可根据需要存放在项目目录或 Brain 目录中。

## 文档创建提醒

-   创建或更新重要文档后，请明确告知用户文件的路径。
-   复杂功能开发强烈建议遵循 **Planning -> Execution -> Verification** 的 Agentic 流程，确保需求清晰、设计合理。

# Claude 101

* **Effective Prompt**: For each prompt you should setting the stage, defining the task, and specifying rules.

* **Important fundamentals**: In order to achive maximum effiency to use Claude, you should respected these points:

```
    1. Delegation - Understand your goals and AI capabilities.
    2. Description - Clearly defining outputs, AI processes and behaviors.
    3. Discernment - Critically evaluating AI outputs.
    4. Diligence - Using AI responsibly and ethically.
```

* **Delegation <-> Diligence Loop**: The goal of this simple process is to test the AI's capabilities, to choose whether we should delegate or not:
```
    1. Identify, and analyze your tasks
    2. Find past data with your final result
    3. Test with AI to replicate the result 
    4. Identify gap, refine and try again.
```

* **Chat, Cowork, Code**: Each mode serves for specific purposes:

```
    1. Chat: Quick, Simple, Drafting, Exploring ideas.
    2. Cowork: Complex task, Analyze, File access.
    3. Code: Technical, Codebased, Building software.
```

* **Projects**: For more complex goal or list of tasks, ultilize ***projects***, in which all content and data are grouped into one place. However make sure, you make everthing clear through ***naming*** and ***specifies detail*** that you give to the AI.

* **Artifacts**: These are more complex and big chunk of the result generated my Claude, you can share, edit, and refine these result within the artifact.

* **Skills**: These tell how Claude should execute a task—the specific steps, order of operations, and methodology you want followed every time. Skills shine when you have **repeatable workflows** you want Claude to run consistently.

* **Connectors**: Let Claude extend it permission to connect, contact and interact with other tools, platforms, and information that ***you allocated*** it to be.

* **Deep Research**: This mode should be used when you are facing complex problem, that need logical, deep reasoning,and that draws from multiple sources. In addition, when using please at least have information to cover these points:

```
    1. Be specific about your goals.
    2. Specify the sections or structure you want.
    3. Include relevant constraints.
    4. Ask Claude to help refine your prompt.
```

* Claude's other usage: There are many other usage but noticed Claude can be ***In Excel***, ***In Word***, ...

<br>

# Claude Code

* **How it works**: These basic points are the core aspects how Claude Code run:

```
    1. Agentic Loop: Gather context -> Take action -> Verify Result.
    2. Context Window: Stored information on the process.
    3. Tools: variety of predefined actions that Claude can ultilize.
    4. Permission Modes: Auto-accept, Plan mode. (Shift + tab)
```

* **Workflow**: ***Explore -> Plan -> Code -> Commit***. Suggesting extend Claude's interaction on tools so that i can test the generated code.

* **Context Management**: ***/compact /clear /context*** but most important be ***specific***, since confusing Claude will look around for information. ***Using Skills, Turn off MCP, Using sub agents***.

* **Review with a Subagent**: Before you push your code, you can ask Claude to use a subagent to review your changes.

```
/commit-push-pr - skill handles the commit, push, and PR creation all in one step.

claude -from-pr [PR_NUM] - to resume work on a PR later.
```

* **CLAUDE.md**: this file is project brief, put it in the root folder. If an rule applies to almost every task you do in that codebase, it belongs here.Suggesting start with an empty Claude.md file.

```
    => CLAUDE.md is pinned to memory. The moment you start a terminal session, the AI reads your root CLAUDE.md and keeps it at the top of its mind for the entire conversation. Because it is always loaded, you must keep it lean.
```

* **SKILL.md**: this file contains procedures / step by step guide on how to do a specific action. ***Called automatically*** when Claude need them. They are straight forward, and the tools' detail seperated from Context Window, saving memory. (Only ***name and description are saved*** inside Context Window)

* **Sub Agents**: It's all about ***Context Window***, sub agent will have it own context window, seperated from the main context window. Then it return the ***summarized result*** to the Main Agent, cutting the context window memory. There are General, Search, Plan, and Customized subagents.

* **Model Context Protocol (MCP)**: is an open standard that lets Claude Code connect to external tools and data sources.

```
    1. Command: claude mcp add
    2. There are: Local, User, Project MCPs.
    3. Context Usage !!!: Keep in mind that unused tools' description may get imported into your Context Window.
```

* **Hooks**: These are ***HARD rules*** that Claude ***HAVE to follow***. Deep dive into coding to tell exactly what Claude have to do, cannot do, how to do,...
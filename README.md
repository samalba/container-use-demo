# Container-Use Demo

Simple demo of Web development with Claude and Container-Use

## Visual demo

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/jFW12iXGy0Q/0.jpg)](https://www.youtube.com/watch?v=jFW12iXGy0Q)

## Demo

Install container-use

```
brew install dagger/tap/container-use
```

Configure Claude to use container-use as an mcp server

```
claude mcp add container-use -- container-use stdio
```

Restrict Claude to only use container-use environments:

```
claude --allowedTools mcp__container-use__environment_checkpoint,mcp__container-use__environment_create,mcp__container-use__environment_add_service,mcp__container-use__environment_file_delete,mcp__container-use__environment_file_list,mcp__container-use__environment_file_read,mcp__container-use__environment_file_write,mcp__container-use__environment_open,mcp__container-use__environment_run_cmd,mcp__container-use__environment_update
```

Try with this prompt:

```
I want to try some new themes for the website. Can you create two new versions of the site in their own environments: one with a dark theme and one with a purple gradient. Run both versions when they are done and give me the URLs.
```

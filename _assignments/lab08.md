---
layout: assignment
due: 2025-04-22 23:59:59 -0700
github_url: https://classroom.github.com/a/FC3GUHH3
published: true
---

## Background

1. For this assignment, you will use [Cursor](https://www.cursor.com/) to build a web UI on top of your lab07 solution
1. Since Cursor uses [Anthropic Claude Sonnet](https://www.anthropic.com/claude/sonnet), you'll need to set up an API key put it in your environment, just like you did for OpenAI. 
1. You'll need to give them a payment method, but it should cost less than $1 to develop this lab.
1. Please call your API key `ANTHROPIC_API_KEY` so we can grade everyone's work using the same setup.

## Objective

1. You will use aider to add a web server (HTTP `Handle`, `ListenAndServe` etc.) to your project06 solution
  - Cursor can replace your input loop (`io.Scanner` etc.) if you wish. You don't need to keep both
  - Cursor can develop a web page which can accept user prompts and chat with the LLM
  - Cursor can reuse your chat code to call OpenAI to answer the same kinds of questions that your project06 solution answers.
1. Feel free to use your own creativity to prompt Cursor to make an attractive web app. Some ideas:
  - Appearance similar to other chat apps
  - Light/dark mode
  - Spinner while waiting for OpenAI
  - Theme in the style of ... 
1. You should do as little manual coding and fixing as possible. Prompt Cursor to do the work.

## Rubric

1. 80 pts - Something runs
1. 20 pts - Attractive and useful

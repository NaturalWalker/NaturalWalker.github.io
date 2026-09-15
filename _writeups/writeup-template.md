---
title: "Writeup template — challenge name"
date: 2026-03-06
description: "A copy-me structure for a CTF writeup: overview, recon, analysis, solution, flag, takeaways."
event: "CTF name YYYY"
platform: "Hack The Box"
category: "rev"        
difficulty: "medium"       
points: 300
tags: [template, reversing]
---

## Overview

One paragraph: what the challenge gives you (a binary, a URL, a capture) and the
goal. Note anything the description hints at.

## Recon

The commands you ran first and what they told you. Keep the output short.

```bash
file ./challenge
strings -n 6 ./challenge | head
```

## Analysis

The core of the writeup: what you found and *how you understood it*. Walk the
reader through your reasoning — the wrong turns are often the useful part.

```c
// reconstructed logic that gates the flag
if (transform(input) == expected) win();
```

## Solution

The steps that produce the flag, in order. A short, self-contained script is
fine; explain what each part does.

```python
# solve.py — outline
expected = bytes.fromhex("....")
print(bytes(b ^ 0x2a for b in expected).decode())
```

## Flag

```text
CTF{example_flag_replace_me}
```

## Takeaways

Two or three lines: the technique this taught you, a tool worth remembering, or
what you'd try first if you saw a similar challenge again.

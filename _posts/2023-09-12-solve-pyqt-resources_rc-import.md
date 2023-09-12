---
title: "Solve resource import errors with pyqt"
tags: [pyqt, Qt, python]
description: "A simple way to solve a common import error when working with pyqt and resource files."
---

## Fixing Import Issues in PyQt's pyuic5-generated Files

When working with PyQt, a common task is converting designer `.ui` files to Python code. This task is typically done using the `pyuic5` tool. However, depending on your project's structure and where you place your generated files, you might run into import issues, especially with the generated `resources_rc.py` file.

### The Problem:

After running `pyuic5`, the generated Python code may contain a line similar to:
\```python
import resources_rc
\```
This line imports resources (icons, images, etc.) that are used in your application. However, if your project structure is modular and relies on relative imports, this direct import can lead to the dreaded `ModuleNotFoundError`.

### The Solution:

Instead of spending time fixing imports manually or writing post-processing scripts, there's a simple switch available in `pyuic5` that rectifies this problem right at the source. Enter `--from-imports`.

When you're converting your `.ui` file to Python, use the following command:
\```bash
pyuic5 your_file.ui -o generated_ui.py --from-imports
\```
By adding the `--from-imports` switch, the generated Python file will use:
\```python
from . import resources_rc
\```
This relative import is often more compatible with modular project structures, ensuring that the generated code works seamlessly without further modifications.

### Conclusion:

The tools we use often have little-known switches or options that can save us a lot of time and headaches. The `--from-imports` switch in `pyuic5` is a great example. Always refer to tool documentation or help menus to uncover such helpful features. With the right switches, you can streamline your development process and focus on what truly matters: building your application.

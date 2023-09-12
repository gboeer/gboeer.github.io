---
title: "Solve resource import errors with pyqt"
tags: [pyqt, Qt, python]
description: "A simple way to solve a common import error when working with pyqt and resource files."
---

## Fixing Import Issues in PyQt's pyuic5-generated Files

When working with PyQt, a common task is converting designer `.ui` files to Python code. This task is typically done using the `pyuic5` tool. However, depending on your project's structure and where you place your generated files, you might run into import issues, especially with the generated `resources_rc.py` file.

## Utilizing PyQt's Resource System with `.qrc` Files

While PyQt provides a robust UI design capability with `.ui` files, it also offers a resource system for embedding images, icons, and other assets directly into your application. This ensures that your PyQt applications remain portable and can be run on various systems without the need to manage external assets separately.
PyQt's resource system simplifies the management of assets in your applications. By leveraging `.qrc` files and tools like `pyrcc5`, you can encapsulate your application assets within the code, ensuring portability and reducing external dependencies. This, combined with the powerful UI capabilities of PyQt, allows developers to create robust and self-contained desktop applications with ease.

### What is a `.qrc` File?

A `.qrc` file, or a Qt Resource Collection file, is an XML-based file that lists resources (like images or icons) in a structured manner. These resources are then compiled into a Python module, which can be imported directly into your PyQt application.

A typical `.qrc` file looks something like this:
```xml
<RCC>
    <qresource prefix="/images">
        <file>path/to/image1.png</file>
        <file>path/to/image2.jpg</file>
    </qresource>
</RCC>
```
In the above structure, the `<qresource>` tag defines a prefix, essentially a virtual path. Inside this tag, each `<file>` tag denotes the path to a resource relative to the `.qrc` file.

### Generating Python Modules from `.qrc` Files using `pyrcc5`

Once you've defined your resources in a `.qrc` file, the next step is to compile this into a Python module. This is where `pyrcc5` comes into play.

To generate a Python resource module, run:
```bash
pyrcc5 resources.qrc -o resources_rc.py
```
This command reads the `resources.qrc` file, compiles the listed resources, and then produces a `resources_rc.py` module.

### Integrating the Resource Module in Your Application

Once `resources.py` is generated, you can directly use the assets in your PyQt code. For instance, if you have an image `image1.png` listed in your `.qrc` file under the prefix `/images`, you can reference it in your application as:

```python
icon = QIcon(":/images/image1.png")
```

### The Problem:

After running `pyuic5`, the generated Python code may contain a line similar to:
```python
import resources_rc
```
This line imports resources (icons, images, etc.) that are used in your application. However, if your project structure is modular and relies on relative imports, this direct import can lead to the dreaded `ModuleNotFoundError`.

### The Solution:

Instead of spending time fixing imports manually or writing post-processing scripts, there's a simple switch available in `pyuic5` that rectifies this problem right at the source. Enter `--from-imports`.

When you're converting your `.ui` file to Python, use the following command:
```bash
pyuic5 your_file.ui -o generated_ui.py --from-imports
```
By adding the `--from-imports` switch, the generated Python file will use:
```python
from . import resources_rc
```
This relative import is often more compatible with modular project structures, ensuring that the generated code works seamlessly without further modifications.

### Conclusion:

The tools we use often have little-known switches or options that can save us a lot of time and headaches. The `--from-imports` switch in `pyuic5` is a great example. Always refer to tool documentation or help menus to uncover such helpful features. With the right switches, you can streamline your development process and focus on what truly matters: building your application.

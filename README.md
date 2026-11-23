# Starfield Papyrus Tool

A modern, cross-platform (Windows / Linux / macOS) GUI for batch compiling and decompiling **Starfield Papyrus** scripts (`.pex` ↔ `.psc`).

This tool wraps proven CLI utilities (Champollion and PapyrusCompiler) in a clean and fast user interface, eliminating the need for `.bat` files.

## Features

- **Decompilation:** Convert `.pex` → `.psc` using **Champollion**.
- **Compilation:** Convert `.psc` → `.pex` using **PapyrusCompiler** (from Creation Kit) or **Caprica**.
- **Batch Processing:** Support for single files, multiple files, or processing an entire directory automatically.
- **Starfield Post-processing:** Automatic cleanup of decompiled scripts (stripping BOM, normalizing line endings, warning on `Guard` and `Struct` blocks).
- **Settings Memory:** Tool paths and import directories are saved between sessions.
- **Clean UI:** Built on modern Qt6 (PySide6).

## Requirements

- **Python 3.10+**
- **Champollion** (v1.3.2+, supports Starfield) – [GitHub Orvid/Champollion](https://github.com/Orvid/Champollion)
- **PapyrusCompiler** (from official Starfield Creation Kit) *or* **Caprica** – [GitHub Orvid/Caprica](https://github.com/Orvid/Caprica)
- **Extracted vanilla scripts** (Import directory) – copy from `Starfield\Tools\ContentResources.zip` to `Starfield\Data\Scripts\Source`.

## Installation from Source

```bash
git clone https://github.com/your-username/starfield-papyrus-tool.git
cd starfield-papyrus-tool

# Create a virtual environment (recommended)
python -m venv .venv
.venv\Scripts\activate   # Windows
source .venv/bin/activate # Linux/macOS

# Install dependencies and the app
pip install -e .

How to use
Run the app with sf-papyrus-tool or python -m sf_papyrus_tool.

In the Tool paths section, set the paths to your tools:

Champollion: Path to champollion.exe.

Compiler: Path to PapyrusCompiler.exe (e.g., ...\Steam\steamapps\common\Starfield\Tools\Papyrus Compiler\PapyrusCompiler.exe).

Compiler type: Choose PapyrusCompiler (Creation Kit) or Caprica.

Import dir: Directory with extracted vanilla .psc scripts (required for compilation).

In the Files / Batch Processing section:

Choose the mode (Single File / Multiple Files / Whole Directory).

Select the source file/folder and the output folder.

Click Decompile or Compile and monitor the progress in the log window.
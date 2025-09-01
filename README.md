# Debian-Python-create-venv
How to install things temporarily for use with Python by using a virtual environment

Here’s how you can set up and use a **Python virtual environment (`venv`) on Debian**, install `pip`, and work with packages like `python-pptx`:

---

## 1. Make sure Python and venv are installed

Debian sometimes splits things into separate packages.

```bash
sudo apt update
sudo apt install python3 python3-venv -y
```

* `python3-venv` → allows you to create virtual environments

---

## 2. Create a new virtual environment

Choose a directory where you want the environment to live. For example, in your home directory:

```bash
python3 -m venv ~/myenv
```

This creates a folder `myenv` containing an isolated Python installation.

---

## 3. Activate the environment

To use it, you need to activate it:

```bash
source ~/myenv/bin/activate
```

You should now see `(myenv)` at the start of your shell prompt.

---

## 4. Install Python and pip (optional but recommended)

Inside the venv:

```bash
* `python3` → the Python interpreter
* `python3-pip` → installs `pip` globally (but each venv will also get its own pip)
```

---

## 5. Install `python-pptx` for example

Now you can install the PowerPoint package (and any others):

```bash
pip install python-pptx
```

---

## 6. Verify installation

You can test in Python:

```bash
python
>>> import pptx
>>> pptx.__version__
```

If you see a version number, it worked.

---

## 7. Deactivate when finished

When you’re done working in the venv:

```bash
deactivate
```

---

✅ You now have an isolated environment with `pip` and can use packages like `pptx`.
This prevents conflicts with system packages and is the recommended way to manage dependencies on Debian.

---

Would you like me to also show you how to **freeze requirements** into a `requirements.txt` so you can easily recreate the environment later?

# Computational Theory Assessment

This repository contains my submission for the Computational Theory module assessment. It consists of a Jupyter Notebook (`problems.ipynb`) that explores the key components of the SHA-256 cryptographic hash algorithm, as defined in the [Secure Hash Standard (FIPS 180-4)](https://nvlpubs.nist.gov/nistpubs/fips/nist.fips.180-4.pdf).

The notebook builds the **SHA-256 algorithm from scratch**, demonstrating an understanding of the underlying theory by implementing the bitwise operations, constants generation, message padding, and final hash computation.

---

## Repository Contents

- `problems.ipynb`: The main notebook containing the solutions to the 5 assessment problems.
- `common_10000_passwords.txt`: A dataset of common passwords used for the dictionary attack demonstration in Problem 5.
- `requirements.txt`: A list of Python packages required to run the code (only **NumPy** is needed).
- `.gitignore`: Specifies files to be ignored by Git.
- `.python-version`: The version of Python (**3.12.1**) used to ensure the reproducibility of the environment.

---

## Installation

### Recommended Setup: GitHub Codespaces

The easiest way to run this assessment with minimal effort is using a GitHub Codespace:

1.  Navigate to the repository, click the **Code** button, select the **Codespaces** tab, and click **+ New codespace**.
2.  The environment will automatically set the Python version and install dependencies from `requirements.txt`.
3.  **Note:** If prompted, ensure the **Python** and **Jupyter** VS Code extensions are installed.
4.  Open `problems.ipynb` and ensure the **Python 3.12.1** kernel is selected before running.

### Local Setup

To set up the repository locally:

1.  **Clone the Repository:**
    ```bash
    git clone https://github.com/MatthewMcCarthy1/computational-theory.git
    cd computational-theory
    ```

2.  **Create and Activate a Virtual Environment:**
    The use of a virtual environment is strongly recommended to isolate dependencies. The repository's `.python-version` file specifies Python 3.12.1.

    ```bash
    # Create the environment
    python3 -m venv venv 

    # Activate the environment (Linux/macOS)
    source venv/bin/activate
    
    # Activate the environment (Windows PowerShell)
    # .\venv\Scripts\Activate
    ```

3.  **Install Dependencies:**
    With the virtual environment active, install the required packages (NumPy and JupyterLab):
    ```bash
    pip install -r requirements.txt
    ```

4.  **Launch the Notebook:**
    ```bash
    jupyter lab
    ```

5.  Open `problems.ipynb` and ensure the kernel is set to the **Python 3.12.1** environment.

---

## Notebook Structure

- **Problem 1**: Binary Words and Operations.  
- **Problem 2**: Fractional Parts of Cube Roots.
- **Problem 3**: Message padding and block parsing according to FIPS 180-4.
- **Problem 4**: The complete hash computation function.
- **Problem 5**: A practical demonstration of a dictionary attack and a discussion on modern, secure password hashing (e.g., Argon2, scrypt).

---

## References

**General Citation Strategy:**
A comprehensive list of all external sources and implementation details is provided via in-text citations and links within the `problems.ipynb` notebook. To keep this `README` focused on the project's core foundations, only the primary standards and required technical documentation are listed below.

- **FIPS 180-4 (Secure Hash Standard):** This is the foundational government standard that defines the complete SHA-256 algorithm implemented in this assessment.
    * National Institute of Standards and Technology (NIST). (2015). *Secure Hash Standard (SHS)* (FIPS PUB 180-4). https://nvlpubs.nist.gov/nistpubs/fips/nist.fips.180-4.pdf
- **NumPy Documentation:** The SHA-256 specification requires precise 32-bit arithmetic. This documentation was used to ensure the correct handling of unsigned 32-bit integers (`uint32`) necessary for accurate word operations.
    * NumPy Developers. (2024). *NumPy Documentation*. https://numpy.org/doc/2.3/user/index.html#user

--- 
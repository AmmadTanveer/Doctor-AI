# Doctor-AI
Rag based health care chatbot to assist patients. 

# How to run ?

## STEPS:

Clone the repo

```bash
git clone https://github.com/AmmadTanveer/Doctor-AI.git
cd Doctor-AI
```

### Step 1: Create conda environment

```bash
conda create -n docai python=3.10 -y
```

### Step 2: Activate conda environment

#### On Windows (PowerShell):
If `conda activate docai` is not working, you have two options:

**Option A: Initialize conda in PowerShell (Recommended)**
```powershell
conda init powershell
```
Then close and reopen PowerShell, or run:
```powershell
. $PROFILE
```

Then activate the environment:
```powershell
conda activate docai
```

**Option B: Use Anaconda Prompt**
- Open "Anaconda Prompt" from the Start Menu
- Navigate to the project directory
- Run `conda activate docai`

#### On Linux/Mac:
```bash
conda activate docai
```

### Step 3: Install dependencies

```bash
pip install -r requirements.txt
```

### Troubleshooting:

If `conda activate docai` is not working on Windows PowerShell:

**Quick Fix:**
1. Load the conda profile manually:
   ```powershell
   . "C:\Users\$env:USERNAME\Documents\WindowsPowerShell\profile.ps1"
   ```
   Or if that doesn't work, try:
   ```powershell
   & "C:\Users\$env:USERNAME\anaconda3\Scripts\conda.exe" "shell.powershell" "hook" | Invoke-Expression
   ```

2. Then activate the environment:
   ```powershell
   conda activate docai
   ```

**Permanent Fix:**
1. Restart PowerShell completely (close and reopen)
2. The profile should load automatically on startup
3. If it still doesn't work, check execution policy:
   ```powershell
   Get-ExecutionPolicy
   ```
   If it's "Restricted", change it:
   ```powershell
   Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
   ```

**Alternative Solutions:**
- Use Anaconda Prompt instead of PowerShell (usually works without issues)
- Verify environment exists: `conda env list`
- Check if conda is installed: `conda --version`

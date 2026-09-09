# Publish this repository

Create an empty public GitHub repository named `networking-study-bank`, then run these commands from this directory:

```powershell
git init
git add .
git commit -m "Initial networking study bank"
git branch -M main
git remote add origin https://github.com/yushi0405/networking-study-bank.git
git push -u origin main
```

After the first push, open the Actions tab and confirm that the StudyCI workflow succeeds.

A useful follow-up PR is to add Japanese translations under `questions/ja/` while keeping the original English set under `questions/en/`.

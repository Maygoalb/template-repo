---
## First Step:
run 
```bash 
pre-commit install -f
```

## 🛠️ Troubleshooting

### Windows: "cannot spawn .git/hooks/pre-commit: No such file or directory"
This happens on Windows when the hook file is incompatible. Fix it by running:

```bash
Remove-Item ".git\hooks\*" -Force
pre-commit install -f
```

### Windows: "OSError: [WinError 193] %1 is not a valid Win32 application"
This happens when an old broken hook is conflicting. Fix it by running:

```bash
Remove-Item ".git\hooks\*" -Force
pre-commit install -f
```

Then try your commit again:
```bash
git commit -m "your message"
```

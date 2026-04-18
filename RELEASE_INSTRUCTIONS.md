# 📦 GitHub Release Instructions

## 🎯 Release Preparation

### 1. Update version in code

**In `updater.py`:**
```python
CURRENT_VERSION = "5.5.1"  # Change to new version
```

**In `index.html` (About section):**
```html
<div class="about-version">5.5.1</div>  <!-- Change version -->
```

### 2. Update CHANGELOG.md

Add new section with changes:

```markdown
## [5.5.1] - 2026-04-20

### Added
- New feature X
- Improvement Y

### Fixed
- Bug Z
```

### 3. Compile the program

Use PyInstaller or other tool:

```bash
pyinstaller --name="CryptoSignal" --onefile --windowed main.py
```

### 4. Create archive

**Archive structure:**
```
CryptoSignal_PRO_v5.5.1.zip
├── CryptoSignal.exe
├── assets/
│   ├── logo.png
│   └── license-content.js
├── README.txt
└── LICENSE.txt
```

**README.txt:**
```
CryptoSignal PRO v5.5.1 BETA

Installation:
1. Extract archive
2. Run CryptoSignal.exe
3. Wait for loading

Support: cryptosignalc@gmail.com
```

---

## 🚀 Creating GitHub Release

### Step 1: Go to Releases

1. Open repository: https://github.com/cryptosignalc-cloud/cryptosignal-pro
2. Click **"Releases"** tab
3. Click **"Create a new release"** or **"Draft a new release"**

### Step 2: Fill the form

**Tag version:**
```
v5.5.1
```
Important: always start with `v`

**Release title:**
```
CryptoSignal PRO v5.5.1 BETA
```

**Description (example):**
```markdown
## 🎉 What's New in v5.5.1

### ✨ Added
- Automatic update check on startup
- New modal window for update downloads
- Improved API error handling

### 🐛 Fixed
- Funding Rate display bug
- Data caching issue
- Win Rate calculation error

### 📊 Improvements
- Faster data loading (30% improvement)
- Memory usage optimization
- Enhanced stability

---

## 📥 Installation

1. Download `CryptoSignal_PRO_v5.5.1.zip`
2. Extract archive
3. Run `CryptoSignal.exe`

## ⚠️ Important

- Trial period: 150 hours of active use
- Requires stable internet connection
- This is a BETA version - may contain bugs

## 🔄 Updating from Previous Version

If you're using v5.5.0:
- Simply download the new version
- Your settings and journal will be preserved

---

**⚠️ NOT FINANCIAL ADVICE. Trade at your own risk.**

© 2024-2026 CryptoSignal PRO
```

### Step 3: Upload files

1. Click **"Attach binaries by dropping them here or selecting them"**
2. Upload `CryptoSignal_PRO_v5.5.1.zip`
3. Optional: upload additional files (README, screenshots)

### Step 4: Publish

1. Review all data
2. If ready to publish:
   - ✅ **"Publish release"** - publish immediately
3. If not ready yet:
   - 📝 **"Save draft"** - save as draft

---

## 🔍 Verify Release

After publishing:

1. **Check link:**
   ```
   https://github.com/cryptosignalc-cloud/cryptosignal-pro/releases/tag/v5.5.1
   ```

2. **Test download:**
   - Download .zip file
   - Verify everything works
   - Run the program

3. **Check auto-update:**
   - Run previous version (v5.5.0)
   - Program should show update notification
   - Click "Download" - should open release page

---

## 📋 Pre-Release Checklist

- [ ] Updated version in `updater.py`
- [ ] Updated version in `index.html`
- [ ] Added section to `CHANGELOG.md`
- [ ] Program compiled
- [ ] .zip archive created
- [ ] Tested on virtual machine
- [ ] README.txt included in archive
- [ ] LICENSE.txt included in archive
- [ ] GitHub Release created
- [ ] .zip uploaded
- [ ] Description filled
- [ ] Release published
- [ ] Link works
- [ ] Auto-update works

---

## 🎓 Useful Tips

### How to Delete a Release
If something went wrong:
1. Releases → click on release
2. Click "Delete" (red button)
3. Confirm deletion
4. Create new release

### How to Edit a Release
1. Releases → click on release
2. Click "Edit" (pencil icon)
3. Make changes
4. "Update release"

### Versioning
- `v5.5.0` → `v5.5.1` - bug fixes
- `v5.5.0` → `v5.6.0` - new functionality
- `v5.5.0` → `v6.0.0` - major changes

---

## ❓ Troubleshooting

**Program doesn't see updates:**
- Check that `updater.py` is included
- Check internet connection
- Look at console for errors

**Download link doesn't work:**
- Check that .zip file is uploaded
- Look at Assets section in release
- File might still be processing by GitHub

**API rate limit:**
- GitHub API has 60 requests/hour limit
- For authenticated - 5000/hour
- If need more - add GitHub token

---

**© 2024-2026 CryptoSignal PRO**

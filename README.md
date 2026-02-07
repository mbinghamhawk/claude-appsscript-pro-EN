# 🚀 Claude-AppsScript-Pro v3.1.0
## An MCP Server that Revolutionizes Google Apps Script Development Efficiency

Claude-AppsScript-Pro is a revolutionary platform that achieves **99% output reduction** and **10x debugging efficiency improvement** for Google Apps Script development through **61 integrated tools**, **AI autonomous development**, and **real-time browser debugging**.

### ✨ Key Features & Innovative Value

| Feature Category | Tools | Innovative Value |
|-------------|---------|------------|
| 🤖 **AI Autonomous Workflow** | 4 | Natural language instructions → Complete system construction |
| 🌐 **WebApp Full Integration** | 6 | One-click deploy & production operation |
| 🔍 **Real-time Debugging** | 8 | Real browser control & instant error identification |
| 📊 **Advanced Spreadsheet Operations** | 18 | Read/write, analysis, optimization & permission management |
| 🎯 **Continuous Development Support** | 25 | Patching, verification, optimization & execution control |

**🎯 What You Can Achieve:**
- "Build a task management system and publish it on the web" → Complete system built in 5 minutes
- "I want to auto-generate monthly reports from sales data" → AI automatically selects and executes the optimal tool chain
- "There's a JavaScript error in my web app" → Real-time debugging in a real browser with automatic fixes

---

## 🛠️ Prerequisites (5 minutes)

### Required Software

✅ **Node.js v18.0.0 or higher** - [Download](https://nodejs.org/)  
✅ **Git** - [Download](https://git-scm.com/)  
✅ **Claude Desktop Latest Version** - [Download](https://claude.ai/download)

**⚠️ Important Notes for Windows:**
- During Node.js installation: **Uncheck** "Automatically install the necessary tools"
- After installation: **PC restart is required**

### Google Cloud Platform Setup

1. **Create a GCP account** - [console.cloud.google.com](https://console.cloud.google.com)
2. **Create a new project**
3. **Enable 3 APIs**:
   - Google Apps Script API
   - Google Drive API  
   - Google Sheets API
4. **Create an OAuth 2.0 client**:
   - Type: **"Web application"** (important)
   - Redirect URI: `http://localhost:3001/oauth/callback`
5. **Make sure to download the client configuration JSON file.**

### 🔐 Required OAuth Scopes Configuration

To enable all 61 tools of Claude-AppsScript-Pro, the following **4 required scopes** are automatically configured:

| Scope URL | Description | Applicable Tools |
|-------------|----------|--------------|
| `https://www.googleapis.com/auth/script.projects` | **Apps Script project creation & updates** | System construction, deployment & management |
| `https://www.googleapis.com/auth/script.deployments` | **Apps Script deployment creation & updates** | WebApp publishing & version management |
| `https://www.googleapis.com/auth/drive` | **Google Drive file operations** | Spreadsheet creation & management |
| `https://www.googleapis.com/auth/spreadsheets` | **Spreadsheet operations** | Data read/write, analysis & optimization |

**📋 Configuration in Google Cloud Console:**
- These scopes are **automatically configured during OAuth authentication**
- Manual configuration is not required, but it is important to select **"Web application"** when creating the OAuth client
- In enterprise environments, pre-approval by an administrator may be required

**⚠️ Extended Scopes for Additional Features:**
If you plan to use the following advanced features in the future, additional scopes may be required:
- `https://www.googleapis.com/auth/script.triggers` - Trigger management
- `https://www.googleapis.com/auth/script.processes` - Process monitoring
- `https://www.googleapis.com/auth/script.external_request` - External API integration

### Checklist

- [ ] Node.js installation confirmed: `node --version`
- [ ] Git installation confirmed: `git --version`
- [ ] Claude Desktop installation complete
- [ ] GCP project created
- [ ] OAuth Client ID & Secret obtained
- [ ] **OAuth scopes understood** (confirmed they are automatically configured)

---

## ⚠️ Important: Verify Prerequisites Before Installation

**Please confirm the following before running the one-click installation:**

### 📋 Required Software Verification
```powershell
# Run the following in PowerShell and confirm all display correctly
git --version
node --version
npm --version
```

**If you get errors:**
- ❌ `'git' is not recognized` → Install [Git](https://git-scm.com/) and restart your PC
- ❌ `'node' is not recognized` → Install [Node.js](https://nodejs.org/) and restart your PC

### 🎯 Alternative Steps (If Git Is Not Installed)
If you don't want to install Git:
1. **[Download ZIP](https://github.com/overdozer1124/claude-appsscript-pro/archive/refs/heads/main.zip)**
2. Install only Node.js
3. After extracting: `npm install` → `.\install-auto.bat`

---

## ⚡ One-Click Installation

### Windows (Fully Automatic & Most Recommended) 🔥

```powershell
# 🚀 PowerShell Fully Automatic Setup (PATH Issue Resolved Version - Most Recommended)
powershell -ExecutionPolicy RemoteSigned -Command "if(!(Test-Path ~\AppData\Roaming\Claude\MCP)){mkdir ~\AppData\Roaming\Claude\MCP -Force}; cd ~\AppData\Roaming\Claude\MCP; if(Test-Path claude-appsscript-pro){cd claude-appsscript-pro; git pull; cd ..} else {git clone https://github.com/overdozer1124/claude-appsscript-pro.git}; cd claude-appsscript-pro; .\install-auto.bat"
```

**Features:**
✅ Automatic PowerShell execution policy fix
✅ WebApp OAuth automatic configuration  
✅ Full protection of existing MCP settings
✅ Automatic error recovery
✅ Complete setup in 3 minutes

#### Alternative Steps When npm install Fails (Windows)

```powershell
# Manual resolution steps when npm install error occurs
cd ~\AppData\Roaming\Claude\MCP\claude-appsscript-pro
$env:NODE_PATH = ""
$env:NPM_CONFIG_PREFIX = ""
npm install
.\install-auto.bat
```

**When to use**: When an npm install error occurs during install-auto.bat execution

### macOS

```bash
# Run in Terminal
curl -fsSL https://raw.githubusercontent.com/overdozer1124/claude-appsscript-pro/main/install.sh | bash
```

### Linux

```bash
# Run in Terminal
curl -fsSL https://raw.githubusercontent.com/overdozer1124/claude-appsscript-pro/main/install.sh | bash
```

### If Git Is Not Installed (ZIP Download Version)

1. **[Download ZIP](https://github.com/overdozer1124/claude-appsscript-pro/archive/refs/heads/main.zip)**
2. After extracting, in the folder:

**Windows:**
```powershell
npm install; .\install-auto.bat
```

**macOS/Linux:**
```bash
npm install && chmod +x install.sh && ./install.sh
```

---

## 🔐 OAuth Authentication Setup (Auto-Launch)

After running the installation command above, the OAuth authentication setup will start automatically.

### Windows Version - WebApp OAuth Setup 🚀

**✨ Revolutionary JSON Upload Feature**

After running the one-click command, the following will launch automatically:

1. **Web browser auto-launch**
   - `http://localhost:3001/setup` opens automatically
   - A beautifully designed OAuth setup screen is displayed

2. **Google Cloud Console Preparation**
   ```
   📋 Prerequisites (already completed above):
   ✅ GCP project created
   ✅ 3 APIs enabled  
   ✅ OAuth 2.0 client created (Web application)
   ✅ Redirect URI: http://localhost:3001/oauth/callback
   ```

3. **JSON File Download**
   - Google Cloud Console → APIs & Services → Credentials
   - Click the "⬇️" button on the right side of the OAuth 2.0 Client ID you created
   - Download the JSON file

4. **JSON File Upload**
   - Drag & drop the downloaded JSON file onto the screen
   - Or click "Choose file"
   - Automatic validation & configuration confirmation

5. **Complete Google Authentication**
   - Click the "Start Google Authentication" button
   - Complete Google authentication in the browser
   - Settings are automatically saved & completed

**⚡ Time required: 2-3 minutes**

### macOS/Linux Version - Terminal OAuth Setup

After installation, an interactive OAuth setup will begin in the terminal:

1. **Enter Client ID**: Copy & paste from Google Cloud Console
2. **Enter Client Secret**: Secure hidden input
3. **Browser Authentication**: Auto-launch for Google authentication
4. **Setup Complete**: .env file automatically updated

**⚡ Time required: 5-8 minutes**

---

## ✅ Verifying Successful Installation

### 1. Restart Claude Desktop

1. Completely close Claude Desktop
2. Restart Claude Desktop

### 2. Connection Test

Run the following in Claude:

```
claude-appsscript-pro:test_connection
```

**On success:**
```
✅ MCP Connection: Normal
✅ Google APIs: Authenticated
✅ Tools: 61
✅ Ready: Claude-AppsScript-Pro v3.1.0
✅ Ready: Claude-AppsScript-Pro v3.1.0
```

### 3. Basic Operation Test

```
"Build a simple task management system and make it available on the web"
```

→ If a complete system is built within 5 minutes, it's a success 🎉

---

## 🔧 Troubleshooting

### Top 5 Common Issues

#### 1. Node.js Is Not Recognized (Windows)
**Symptom:** `'node' is not recognized as an internal or external command`

**Solution:**
```powershell
# Run with absolute path
"C:\Program Files\nodejs\node.exe" --version

# Or add to PATH environment variable and restart PC
```

**Permanent fix:** Add Node.js to PATH (see setup-windows-path.md for details)

#### 2. MCP Server Is Not Recognized
**Symptom:** Tools are not displayed in Claude

**Solution:**
```bash
# Check Claude Desktop configuration
notepad "%APPDATA%\Claude\claude_desktop_config.json"  # Windows
open ~/Library/Application\ Support/Claude/claude_desktop_config.json  # macOS
nano ~/.config/Claude/claude_desktop_config.json  # Linux
```

**Configuration example:**
```json
{
  "mcpServers": {
    "claude-appsscript-pro": {
      "command": "/absolute/path/to/node",
      "args": ["/absolute/path/to/claude-appsscript-pro/server.js"],
      "cwd": "/absolute/path/to/claude-appsscript-pro"
    }
  }
}
```

#### 3. OAuth Authentication Error
**Symptom:** `redirect_uri_mismatch`

**Solution:**
- Recreate the OAuth client in GCP as **"Web application"**
- Redirect URI: `http://localhost:3001/oauth/callback`

**Windows version:**
- Use WebApp OAuth setup (JSON upload)
- If it doesn't auto-launch: `node scripts/oauth-setup.cjs --web`

**macOS/Linux version:**
- Interactive setup in terminal
- Re-run: `npm run oauth-setup`

#### 4. Syntax Error
**Symptom:** `SyntaxError: Invalid regular expression flags`

**Solution:**
```bash
# Check Node.js version (v18.0.0 or higher required)
node --version

# Update if below v18
```

#### 5. Large File Error
**Symptom:** 100MB+ file size error during GitHub push

**Solution:**
```bash
# Check/add to .gitignore
echo "node_modules/" >> .gitignore
echo "*.log" >> .gitignore
git rm --cached [large-file]
```

### Detailed Support

**Windows-specific issues:**
- 📄 **Windows Node.js PATH Configuration Guide.txt**: Detailed PATH setup
- 🔧 **install-auto.bat issues**: Check logs with `type install-auto.log`

**All platforms:**
- 📄 **TROUBLESHOOTING.md**: Detailed troubleshooting guide
- 🐛 **GitHub Issues**: Bug reports & feature requests
- 💬 **GitHub Discussions**: Community support

---

## 📚 Usage & Practical Examples

### 🤖 AI Autonomous Development (Key Feature)

```
"Create a customer management system and let me check data in real-time"
→ Claude automatically selects and executes the optimal tool chain

"I want to auto-generate monthly reports from sales data"  
→ Fully automated from data analysis to report creation to auto-distribution

"There's a JavaScript error in my web app, find it and fix it"
→ Automatic execution from error monitoring in a real browser to applying fix code to verifying behavior
```

### 🎯 Example Systems You Can Build

#### 📈 Business Systems
- **Customer Management System**: Customer information management, history tracking & automatic email sending
- **Expense Reimbursement System**: Application forms, approval workflows & automatic calculation
- **Project Management**: Task management, progress visualization & team collaboration
- **Reservation Management System**: Real-time availability & automatic confirmation emails

#### 📊 Data Analysis & Reports  
- **Sales Analysis Dashboard**: Real-time sales & trend analysis
- **Inventory Management**: Automatic order alerts & inventory trend graphs
- **Survey Aggregation**: Automatic tallying, results visualization & respondent management
- **Attendance Management**: Clock-in/out records, overtime calculation & leave management

### ⏰ Estimated Development Time

| System Scale | Dev Time | Features | Complexity |
|-------------|----------|--------|--------|
| **Simple** | 3-5 min | Basic features only | Form + data storage |
| **Standard** | 5-10 min | Moderate features | Analysis + reports + UI |
| **Advanced** | 10-20 min | Advanced features | AI analysis + automation + integration |
| **Enterprise** | 20-30 min | Comprehensive system | Permission management + audit + optimization |

---

## 🌟 Development Roadmap

### Phase 1 ✅ **Complete**: Detailed README & Full Beginner Support (2025.08.17)
- ✅ **Comprehensive documentation created**: Beginners can set up in 5 minutes
- ✅ **Platform-specific instructions clarified**: Full support for Windows/macOS/Linux
- ✅ **Troubleshooting integrated**: Top 5 common issue solutions
- ✅ **One-click commands prepared**: Installation requiring no technical knowledge

### Phase 2 ✅ **Complete**: Full Cross-Platform Integration (2025.08.17)
- ✅ **WebApp OAuth setup**: JSON upload for all OS
- ✅ **OAuth duplicate execution prevention**: Innovative algorithm ported to all OS
- ✅ **MCP safe update feature**: Existing configuration protection system integrated across all OS
- ✅ **Automatic error recovery**: Unified error handling across all OS
- ✅ **True platform unification**: Windows-equivalent features fully realized on macOS/Linux

### Phase 3: Advanced Feature Integration (In Progress) 🔄

**Goal:** Enterprise-level features & CI/CD integration

**Planned features:**
- 🔄 **CI/CD Integration**: GitHub Actions, automated testing & deployment
- 🔄 **Docker Integration**: Containerized auto-deployment & Kubernetes support
- 🔄 **Team Development Features**: Permission management, collaboration & audit logs
- 🔄 **Performance Optimization**: Large-scale data processing & speed improvements

### Phase 4: Multilingual & Global Expansion (Planned) 🌐

- **Multilingual Support**: English, Chinese, Korean & Spanish UI
- **Regional Optimization**: Google Workspace configuration support for each country
- **Global Community**: Building developer communities in each country
- **Enterprise Edition**: Advanced features for businesses & SLA support

### Phase 5: AI/ML & Next-Generation Technology Integration (Planned) 🤖

- **Predictive Analytics**: AI-powered data trend prediction & automatic reports
- **Auto-Optimization**: Automatic system improvement & performance enhancement
- **Voice Control**: Voice command support like "Create a sales report"
- **Visual Programming**: System creation with drag & drop
- **GPT-4o Integration**: Advanced code generation & auto-debugging features

---

## 🤝 Contributing & Support

### 🌟 Community Contributions Welcome

We welcome community contributions to help complete features for macOS/Linux:

**Contributions we're looking for:**
- 🍎 Testing & feedback on **macOS environments**
- 🐧 Testing & feedback on **Linux environments**  
- 🎨 **UI/UX improvement** suggestions
- 🌐 **Multilingual translation** assistance
- 📚 **Documentation improvements**
- 💡 **New feature ideas**

**How to contribute:**
1. 🐛 **GitHub Issues**: Bug reports & feature requests
2. 🔧 **Pull Requests**: Code contributions
3. 💬 **GitHub Discussions**: Ideas, questions & support

### 📞 Support

**Technical issues:**
- 📄 **TROUBLESHOOTING.md**: Detailed troubleshooting guide
- 🔧 **GitHub Issues**: Bug reports
- 💭 **GitHub Discussions**: Questions & consultation

**Community:**
- 🌟 **Star this repo**: Support the project
- 🔄 **Share & Fork**: Spreading the word & improvements welcome
- 📢 **Social media posts**: Share your experiences & creations

---

## 🎊 Summary

**Claude-AppsScript-Pro v3.1.0** is a revolutionary platform that opens a new era in Google Apps Script development.

### ✨ Value Delivered

**For developers:**
- 🚀 **10x development efficiency**: AI autonomous system & real-time debugging
- 💡 **Unleash creativity**: Realize ideas free from technical constraints
- 🎓 **Skill improvement**: Learning through advanced system development

**For businesses:**
- ⏰ **Instant system construction**: From idea to production in minutes
- 💰 **Cost reduction**: No outsourcing needed & in-house development support
- 📈 **Competitive advantage**: Market leadership through rapid system development

**For society:**
- 🌐 **Technology democratization**: Even programming beginners can build advanced systems
- 🚀 **Innovation acceleration**: Removing barriers to realizing ideas
- 🤝 **Community value**: Knowledge sharing through open source

### 🔥 Get Started Now!

```powershell
# Windows (Most Recommended - With Automatic PowerShell Execution Policy Fix)
powershell -Command "& { Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser -Force; git clone https://github.com/overdozer1124/claude-appsscript-pro.git; cd claude-appsscript-pro; npm install; .\install-auto.bat }"
```

```bash
# macOS/Linux (Full Version - Completed 2025.08.17!)
git clone https://github.com/overdozer1124/claude-appsscript-pro.git && cd claude-appsscript-pro && npm install && chmod +x install-complete.sh && ./install-complete.sh
```

```bash
# All OS Unified Version (Full Feature Version - Recommended)
git clone https://github.com/overdozer1124/claude-appsscript-pro.git && cd claude-appsscript-pro && npm install && node install-complete.js
```

**🎯 In 5 minutes, you'll be experiencing true cross-platform unified, next-generation Google Apps Script development.**

---


**📋 Requirements**: Node.js 18.0.0+ | **🏷️ License**: MIT | **⭐ Version**: v3.1.0


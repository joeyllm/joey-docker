# 🐳 Joey Docker

Dockerfiles + deployment configs for **Joey LLM** 🦘  
This repo centralises all container builds so our systems stay **consistent, reproducible, and ready for deployment** 🚀  

---

## 📂 What’s Inside

- 🖥️ **System** → base OS + core dependencies  
- 🤖 **Model Base** → training + inference environments  
- 📊 **JupyterHub** → multi-user notebooks for data + experiments  
- 🌐 **Web** → API + frontend containers  
- ☸️ **Kubernetes** → manifests + Helm charts for cluster deployment  

---

## ⚡ Why Centralise?
- 🔁 **Consistency** → same build everywhere  
- 🧩 **Modularity** → update one service without breaking others  
- 📦 **CI/CD** → automated builds + pushes via GitHub Actions  
- 👥 **Collaboration** → easier for contributors to jump in  

---

## 🛠️ Usage
Clone the repo:
```bash
git clone https://github.com/joeyllm/joey-docker.git
cd joey-docker
```

Build a specific service:
```bash
docker build -t joeyllm/web ./web
```

Run locally:
```bash
docker run -p 8080:8080 joeyllm/web
```

---

## 🤝 Contributing
- Found a bug? 🐛 Open an **Issue**  
- Have improvements? 🔧 Submit a **PR**  
- Want to help maintain? 🧑‍💻 Join as a **Maintainer**  

---

## 📜 License
Apache 2.0 © Joey LLM

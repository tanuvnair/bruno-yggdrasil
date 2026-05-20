# 🌳 bruno-yggdrasil

A centralized, version-controlled "World Tree" repository for my API collections. Built using **Bruno**, the open-source, Git-friendly alternative to Postman and Insomnia. 

This repository acts as a single source of truth, organizing different development environments into isolated filesystem realms.

---

## 🚀 Local Workspace Setup

Because Bruno treats collections as standard text directories, you do not need to create premium cloud workspaces. Everything runs seamlessly in Bruno's default local workspace.

### 1. Clone the Master Tree
```bash
git clone <your-private-repository-url>
cd bruno-yggdrasil
```

### 2. Connect a Realm to the Bruno Client
1. Launch the **Bruno Desktop Application**.
2. From the home dashboard, click **Open Collection**.
3. Navigate into either the `personal/` or `algorisys/` directory.
4. Select the specific subdirectory containing the target `bruno.json` file (e.g., `algorisys/auth-service`).
5. Click **Open**. Your project will instantly appear in the sidebar.

---

## 🔒 Security & Secret Management

To comply with enterprise security standards and prevent credentials from leaking to remote version control, follow these rules:

1.  **Strictly use local environments:** Always create and save sensitive variables (such as API keys, Bearer tokens, or corporate database secrets) in Bruno's environment settings using the custom local naming scheme.
2.  **Verify Filenames:** Ensure environment-specific secrets are saved under files ending explicitly with `*.local.json`.
3.  **Local Git Safeguard:** The root `.gitignore` is hard-configured to strip `**/.bruno/` cache patterns and all `*.local.json` variants from the tracking staging area.

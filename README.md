# Fajar Siagian Playbook

Reusable deployment playbook for provisioning Laravel applications on **AWS Lightsail** with a hardened LEMP stack — PHP 8.4 from Ondřej PPA, Nginx sourced directly from `nginx.org`, and every script parameterized by `PROJECT_NAME` so you can reuse it across projects without manual find-and-replace.

## Stack

| Layer | Choice |
|---|---|
| OS | Ubuntu 24.04 LTS |
| PHP | PHP 8.4 — Ondřej PPA only |
| Web Server | Nginx stable from official nginx.org |
| Node.js | NVM + npm/pnpm |
| Database | MySQL / MariaDB / PostgreSQL / MongoDB / SQL Server |
| Cache/Queue | Redis + Horizon |
| Debugging | Telescope (staging only) |
| Process Monitor | Supervisor |

## Usage

1. Clone this repo.
2. Open `docs/laravel-lightsail-ondrej-nginx-stable-nvm-pnpm-playbook.html` in a browser.
3. Set your `PROJECT_NAME`, `PROJECT_REPO`, and `PUBLIC_IP` — every snippet uses these variables.
4. Follow the sections in order: Lightsail firewall → server bootstrap → Nginx → PHP → Node.js → database → project deploy.

The playbook is designed so you never hardcode a project name. Change the variables once at the top and every subsequent command adapts automatically.

## Contents

- `docs/` — Full HTML playbook with copy buttons, search, sticky sidebar, and interactive checklist
- `README.md` — This file

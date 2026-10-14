<div align="center">

# Guilherme Kauan Marques

### Software Engineer — Python · Django · PostgreSQL

**I build systems that run real operations.** Production tracking, ERP integrations and internal tools that factories depend on every single day.

<br/>

[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Django](https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white)](https://www.djangoproject.com/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![SQL Server](https://img.shields.io/badge/SQL_Server-CC2927?style=for-the-badge&logo=microsoftsqlserver&logoColor=white)](https://www.microsoft.com/sql-server)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)
[![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)](https://git-scm.com/)

<br/>

📍 **Brazil** · 🕐 **CST / EST friendly** · 🌎 **Open to remote roles (US)**

<br/>

[![Email](https://img.shields.io/badge/Email-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:guilhermekauamt01@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/guilherme-kauan-104546245/)

</div>

---

## What I do

I work as a software engineer in the manufacturing industry, where I own internal systems end to end — from data modelling and API design to deployment and on-the-floor support.

My focus is **backend engineering for operational software**: systems where correctness matters because a person on a shop floor is waiting on the screen, and where a bug stops production rather than annoying a user.

What that has taught me:

- **Designing for non-technical users under pressure.** The best interface for a factory worker is one they cannot get wrong. That constraint has shaped more architecture decisions than any style guide.
- **Integrating with the systems that already exist.** Real companies run on ERPs, legacy databases and spreadsheets. Shipping means meeting them there, not replacing them.
- **Owning the whole path to production.** Linux, Nginx, systemd, TLS, migrations, backups — I deploy and support what I build.

---

## Featured work

### 🏭 Casanova System — Production Management & Traceability

The platform I designed and built to run the production floor of a window and door manufacturer. It tracks every unit from raw material to shipping in real time.

[![Repo](https://img.shields.io/badge/View_repository-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/casanova-system/casanova)

| | |
|---|---|
| **Scale** | ~5,900 lines of Python · 53 routes · 13 domain models · 39 migrations |
| **Stack** | Django 5.2 · PostgreSQL 16 · DRF · Bootstrap 5 · Gunicorn + Nginx |
| **Integration** | Microsoft SQL Server (ERP) via `mssql-django` — live in production |
| **Status** | In production, used daily on the shop floor |

**Engineering problems solved on this project:**

- **A dual-scan workflow that enforces process order.** Each workstation scans twice — once to start work, once to release the unit downstream — so no station can hold production hostage and no step can be skipped. Start and finish are stored with separate user and timestamp fields, because the operator who starts a job is often not the one who finishes it.

- **One label, two scanning technologies.** Every printed label carries a QR Code (structured JSON for phone cameras) and a Code 128 barcode (numeric ID for industrial laser scanners), because workstations have different hardware. A single parser handles both, so the registration flow is identical regardless of device.

- **Internal HTTPS with a private certificate authority.** Browser cameras require a secure context, and an internal network has no public domain to issue a certificate against. I built a company-local CA, signed the server certificate with it, and shipped a per-platform installation flow — unlocking camera scanning without weakening security.

- **A deliberate decision to delete a mobile app.** I removed a working Flutter application in favour of a single responsive web screen, after measuring the trade-off: 41 MB less to load on the factory network, no more iOS service-worker caching delaying fixes, and one codebase instead of two.

---

## Tech stack

<table>
<tr>
<td valign="top" width="33%">

**Languages**

<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" width="38" title="Python"/>
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" width="38" title="JavaScript"/>
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/dart/dart-original.svg" width="38" title="Dart"/>
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/csharp/csharp-original.svg" width="38" title="C#"/>
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/kotlin/kotlin-original.svg" width="38" title="Kotlin"/>

</td>
<td valign="top" width="33%">

**Backend & Data**

<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/django/django-plain.svg" width="38" title="Django"/>
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-original.svg" width="38" title="PostgreSQL"/>
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/microsoftsqlserver/microsoftsqlserver-plain.svg" width="38" title="SQL Server"/>
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg" width="38" title="MySQL"/>
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/redis/redis-original.svg" width="38" title="Redis"/>

</td>
<td valign="top" width="33%">

**Frontend & Mobile**

<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bootstrap/bootstrap-original.svg" width="38" title="Bootstrap"/>
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" width="38" title="HTML5"/>
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" width="38" title="CSS3"/>
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/flutter/flutter-original.svg" width="38" title="Flutter"/>

</td>
</tr>
<tr>
<td valign="top" width="33%">

**Infrastructure**

<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linux/linux-original.svg" width="38" title="Linux"/>
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nginx/nginx-original.svg" width="38" title="Nginx"/>
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg" width="38" title="Docker"/>
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" width="38" title="Git"/>

</td>
<td valign="top" width="33%">

**Also experienced in**

<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/windows8/windows8-original.svg" width="38" title="Windows Server"/>
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg" width="38" title="VS Code"/>

<sub>Delphi (Pascal) · Windows Server · ERP integrations · REST APIs</sub>

</td>
<td valign="top" width="33%">

**Currently exploring**

<sub>System design at scale · Kubernetes · Event-driven architecture · AI-assisted tooling</sub>

</td>
</tr>
</table>

---

## Background

I started in 2022 as an **apprentice**, moved through an **internship**, and now work as a **full-time engineer** — building and maintaining the systems a manufacturing company runs on.

That path gave me something a textbook cannot: I have written **Delphi/Pascal and SQL Server** for enterprise operations, and I have shipped **modern Python/Django** services. I understand both sides of a company's reality — the legacy system that cannot stop running, and the new service that has to earn its place beside it.

Alongside work, I am completing a **Computer Science** degree.

---

## GitHub activity

<div align="center">

<img height="165" src="https://github-readme-stats.vercel.app/api?username=devgui01&show_icons=true&theme=github_dark&hide_border=true&count_private=true&include_all_commits=true" />
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=devgui01&layout=compact&theme=github_dark&hide_border=true&langs_count=8" />

</div>

---

<div align="center">

### Let's talk

I am open to **remote software engineering roles**, and always glad to discuss backend architecture, manufacturing systems or ERP integrations.

<br/>

[![Email](https://img.shields.io/badge/guilhermekauamt01@gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:guilhermekauamt01@gmail.com)
[![LinkedIn](https://img.shields.io/badge/Guilherme_Kauan-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/guilherme-kauan-104546245/)

<br/><br/>

<sub><i>"Systems that run real operations."</i></sub>

</div>

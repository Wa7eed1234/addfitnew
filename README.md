# AddFit membership prototype

Fitness website with member registration, phone/password login, subscription dates and a member dashboard route.

## Run locally

Use Python 3 in an isolated environment. The following dependency list is inferred from source imports; this repository has no tested dependency lockfile.

```bash
python -m venv .venv
# Windows PowerShell: .venv\Scripts\Activate.ps1
# macOS/Linux: source .venv/bin/activate
python -m pip install Flask Flask-SQLAlchemy Flask-Login Flask-Admin requests
python -m flask --app main run --host 127.0.0.1 --port 5000
```

Open http://127.0.0.1:5000. Use only synthetic local records. Complete the known repairs below first; dependency compatibility and full application flows have not been verified.

## Current status and known limitations

Repair main.py: /dashboard renders missing dashboard.html; the uploaded template is templates/dash.html. Hash passwords, restrict Flask-Admin, and replace the development secret before any deployment.

## Review status

Documentation drafted from repository source on 13 September 2026. This review did not run the application or certify it for production.

## Cleanup applied

- Corrected the dashboard route to use the uploaded dash.html template.

The items above supersede the corresponding original review findings. Other listed limitations remain open.

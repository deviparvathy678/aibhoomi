# Streamlit Community Cloud deployment

Use these settings to publish a demo from this repository:

- Repository: `deviparvathy678/aibhoomi`
- Branch: `real-imagery-alerts`
- App file: `app.py`
- Python: 3.12

In Streamlit Community Cloud's advanced settings, add a private secret block for
the first administrator:

```toml
[bootstrap_admin]
username = "choose-an-admin-name"
password = "use-a-unique-password-at-least-12-characters-long"
```

The app creates this administrator only when the database has no users. Keep
the secret out of GitHub and do not share it in screenshots or public messages.

## Demo data only

SmartPanchayat currently stores cases, users, and uploaded comparison evidence
in local SQLite and local files. Streamlit Community Cloud does not guarantee
that local files persist, so this deployment is suitable for a demo only. Do
not enter real citizen, property, or government records. Before operational
use, move the database and uploaded evidence to durable managed storage with
access controls and backups.

# Acres development with Claude Code

Use your personal accounts for GitHub and Google Cloud SSH, plus the Firebase CLI on the same Google account. Claude Code uses those same command-line tools. A Codex installation or the company Employee plugin is not required.

Before setup, finish the Hyatus account email sent to **boulderchaim@gmail.com**, accept the **Hyatus-Living/acres** GitHub invitation as **boulderchaim1**. Use that Gmail account for Google Cloud. Google Cloud access is assigned directly, without a separate invitation email.

Paste the following prompt into Claude Code on your computer. Browser sign-ins, consent, and any passkey checks must be completed using your own accounts.

```text
Set up my computer for Acres development and verify the real connections. I am Chaim, boulderchaim@gmail.com, GitHub boulderchaim1.

Use my own native GitHub CLI, Google Cloud CLI/SSH, and Firebase CLI credentials. I do not need Codex or the private Hyatus Employee plugin for these tasks. Never request or copy Michael's credentials, service-account keys, or another employee's tokens. Preserve any existing unrelated accounts, configurations, and checkouts. Install missing Git, gh, Node.js, gcloud, and Firebase CLI using supported installers for my operating system. Open the required personal sign-in flows and wait for me to finish any user-only verification.

GitHub:
- Inspect gh auth status and gh api user. The signed-in login must be boulderchaim1. If needed, use gh auth login with GitHub.com, HTTPS, and browser authentication.
- Confirm my accepted permission on Hyatus-Living/acres is MAINTAIN. If the invitation remains pending, guide me to accept it before proceeding.
- Reuse my existing Acres checkout, or clone Hyatus-Living/acres into an ordinary development directory. Work only in that repository. Confirm the origin URL.
- Read the repository's development instructions. Configure this checkout's author email to an email verified on my GitHub account. Set up signed commits, using my own local signing key and GitHub signing-key registration if needed, because the organization requires signed commits. Never overwrite an existing key. Preserve PR protections and required checks. I can create PRs and merge allowed PRs in Acres.

Google Cloud:
- Inspect gcloud config list and gcloud auth list. Use boulderchaim@gmail.com. If it is missing, sign me in with gcloud auth login boulderchaim@gmail.com --no-activate.
- Use explicit --account=boulderchaim@gmail.com --project=hyatus-openclaw --zone=us-central1-a --tunnel-through-iap on compute SSH/SCP commands. Do not switch an unrelated default account or project.
- The dedicated Acres/Arosa VM is openclaw-builder. Connect with:
  gcloud compute ssh openclaw-builder --account=boulderchaim@gmail.com --project=hyatus-openclaw --zone=us-central1-a --tunnel-through-iap
- Verify my own OS Login identity and these scoped commands over SSH:
  sudo -n /usr/local/sbin/acres-server status web
  sudo -n /usr/local/sbin/acres-server status research
  sudo -n -u acres-runtime /usr/local/bin/acres-db chat 'SELECT count(*) AS tables FROM sqlite_master'
- Check schema access to market, knowledge, and ledger too. Verify write-mode connectivity with --write chat 'SELECT 1 AS write_connection', which changes no records. Do not insert, update, delete, or migrate production data during setup.
- The database command accepts chat, market, knowledge, and ledger only. Normal queries are read-only; intentional record or schema edits use:
  sudo -n -u acres-runtime /usr/local/bin/acres-db --write DATABASE 'SQL'
  It executes one SQL statement and commits successful edits. Inspect schema, target rows, and the intended change before a real production edit, then read back the result. Database attachment, arbitrary file paths, extensions, and file-reading SQL functions are unavailable.

Direct production code and service control:
- Use sudo -n /usr/local/sbin/acres-server, not a general sudo shell or Docker access.
- Read production web code with:
  sudo -n /usr/local/sbin/acres-server read web app-starter/server.js
- Read production research code with:
  sudo -n /usr/local/sbin/acres-server read research service.mjs
- The web target accepts source paths beginning app-starter/ or acres-research/. The research target uses paths relative to the deployed research directory, such as service.mjs or skills/NAME/SKILL.md. For example, repository acres-research/service.mjs maps to research service.mjs.
- To apply an intentional code change, inspect the live file, edit and validate the matching local source, then send its bytes over SSH stdin to:
  sudo -n /usr/local/sbin/acres-server write TARGET SOURCE_PATH
  For example, redirect local app-starter/public/app.js into the gcloud SSH command whose remote command is 'sudo -n /usr/local/sbin/acres-server write web app-starter/public/app.js'. Keep file content out of shell interpolation.
- Restart only the affected Acres service:
  sudo -n /usr/local/sbin/acres-server restart web
  sudo -n /usr/local/sbin/acres-server restart research
  Restart queues the operation. Check status, the actual application response, and scoped logs before reporting success. Research may drain active work before restarting.
- Use 'logs web' or 'logs research' for the corresponding application logs. Do not print credentials from logs.
- Web edits persist across restarts and image releases as source overrides. After the change is included in a deployed image, use 'reset web SOURCE_PATH' to remove that override and restart onto the image's version. Research edits are live files and must also be recorded in Git so a later deployment preserves them. Keep production changes reconciled with an Acres branch/PR.
- Host configuration, deployment scripts, secrets files, unrelated services, and the shared production Git checkout remain administrator-managed. The application runs with its existing Acres runtime credentials.

Public site (Firebase Hosting):
- The Acres public website is site/ in the Acres repository, hosted on Firebase Hosting in the Google Cloud project hyatus-openclaw (site hyatus-openclaw). The main application at build.witharosa.ai (also app.witharosa.ai) runs on Google Cloud too; nothing Acres needs a Vercel account. Vercel was fully retired on 2026-10-28: the arosa-site project and its domain record were deleted and site/vercel.json was removed, so never run vercel commands or look for Vercel deployments. firebase.json rewrites /api/** to the arosa-site-proxy Cloud Run service (site/proxy/), which passes only /api/public/stats and /api/public/beta-apply through to the app; see site/README.md.
- Work on a branch and open a PR. Before opening it, run npm run check and the serial node suite, which is the acceptance gate: node --test --test-concurrency=1 acres-research/*.test.mjs app-starter/tests/*.test.mjs. The parallel runner has known timing flakes; a failure that passes serially and alone is not a regression.
- Run firebase login:list and, if needed, firebase login with boulderchaim@gmail.com. Then run firebase hosting:sites:list --project hyatus-openclaw from site/ and report the result honestly: site deploys are administrator-run until my Firebase Hosting role is granted, so a permission denial there is expected and is not a setup failure. Do not create a project or deploy anything during setup.
- Verify the live site instead: curl -s https://witharosa.ai/api/public/stats returns JSON totals with a fresh updatedAt, https://witharosa.ai loads, and https://arosa-site.vercel.app returns 404.

Finish by reporting what you actually verified: GitHub identity and permission, checkout, commit signing, personal Google account and SSH, all four database connections including harmless write-mode verification, production source access and scoped service status, and the Firebase site check. List any remaining user action precisely. Do not claim access was verified merely because a CLI is installed or an invitation was sent. After setup, use these connections for my Acres development requests.
```

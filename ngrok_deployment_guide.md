# NLC Gate Pass System - Deployment Guide

## One-Time Setup Steps (ngrok Static Domain)
Follow these steps to set up a permanent static URL for the local backend:

1. Sign up at [ngrok.com](https://ngrok.com/) — free account.
2. Go to the ngrok Dashboard → Copy Authtoken.
3. Go to the ngrok Dashboard → **Domains** → Claim 1 free static domain (e.g., `igps-nlc.ngrok-free.app`).
4. Open a terminal and run the following command once to authenticate:
   ```bash
   ngrok config add-authtoken <your_authtoken>
   ```

## Comparison Table

| Solution | Static URL | Free | No Signup | Reliability |
|---|---|---|---|---|
| Cloudflare Tunnel (previous) | ❌ Random every restart | ✅ | ✅ | Medium |
| **ngrok Static Domain (current)** | ✅ Permanent | ✅ | ❌ Needs account | High |
| Serveo SSH Tunnel | ✅ Permanent | ✅ | ✅ | Medium |
| ngrok Paid Plan | ✅ Permanent | ❌ | ❌ | Very High |

**Recommended:** ngrok free static domain — most stable and reliable for internship demo use.

## Verification
To verify the deployment:
1. Run `python app.py`
2. Confirm the console prints the permanent `ngrok-free.app` URL.
3. Stop and restart `app.py` and confirm the exact same URL appears again.
4. Open the GitHub Pages frontend and confirm login works without any code changes.
5. All 4 roles (`employee`, `manager`, `admin`, `security`) should log in and redirect correctly.

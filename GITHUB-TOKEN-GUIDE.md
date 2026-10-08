Here's a focused, short guide covering **only the token setup**.

# GitHub Token Setup Guide (Beginner Friendly)

A short guide to setting up GitHub authentication so you never have to
deal with password errors again.


## ❓ Why Do I Need a Token?

GitHub no longer accepts your account password when you push code
from the terminal. Instead, you must use a *Personal Access Token (PAT)*

A token is basically a one-time password that:

- Is safer than your real password
- Can be revoked anytime without changing your account password
- Can be limited to specific permissions (like push/pull only)

---

## 🔑 Step 1: Create a Personal Access Token

1. Go to GitHub → click your profile picture (top right) → Settings
2. Scroll down to Developer settings (bottom of the left sidebar)
3. Click *Personal access tokens → Tokens (classic)*
4. Click *Generate new token → Generate new token (classic)*
5. Fill in:
   -Note `Ubuntu Laptop` (or any name you'll recognize)
   - Expiration: `90 days` (or `No expiration` for personal machines)
   - Scopes:* check ☑️`repo (this is the only one you need)
1. Scroll down, click Generate token
2. COPY THE TOKEN IMMEDIATELY — you will never see it again

The token looks like this:ghp_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx

---

> ⚠️ **Treat this like a password.** Never share it, never commit it to a repo,
> never paste it in a public chat.

---

## 💾 Step 2: Save the Token (So You Only Type It Once)

Run this **once** in your terminal:

```bash
git config --global credential.helper store

You'll be prompted:

```
Username for 'https://github.com': your-username
Password for 'https://your-username@github.com': [paste the token here]

- **Username:** your GitHub username (e.g., `SidhCodez`)
- **Password:** paste the token (nothing will appear as you paste — that's normal)

Press Enter. The push will succeed, and the token is saved.

---

## ✅ Step 4: Verify It Was Saved

```bash
cat ~/.git-credentials
```

You should see a line like:

```
https://YOUR_USERNAME:ghp_xxxxxxxxxxxx@github.com
```

That means Git remembers your token. **You'll never be asked again.**

---

## 🔒 Step 5: Secure the File

The token is stored in plain text, so restrict who can read it:

```bash
chmod 600 ~/.git-credentials
```

Verify:

```bash
ls -l ~/.git-credentials
```

Expected output:

```
-rw------- 1 your-user your-user ... .git-credentials
```

The `-rw-------` means **only you** can read it.

---

## 🧪 Step 6: Test It Works

Make a tiny change and push:

```bash
echo "test" >> README.md
git add README.md
git commit -m "Test token"
git push
```

If it pushes **without asking for a username or password** — you're done. 🎉

Undo the test change:

```bash
git reset --hard HEAD~1
git push --force
```

---

## ⚠️ If Something Goes Wrong

### Token rejected? ("Authentication failed")

- Make sure you're pasting the **token**, not your GitHub password
- Check the token has the **`repo`** scope
- Token may have expired → create a new one

### Change or revoke a token

1. GitHub → **Settings → Developer settings → Personal access tokens**
2. Find the token → click **Delete** (to revoke)
3. Or click **Regenerate** (to make a new one with the same settings)

After revoking, clear the saved token and re-enter:

```bash
rm ~/.git-credentials
# next push will ask for the new token
```

### Forgot which tokens exist?

Check here anytime:

**GitHub → Settings → Developer settings → Personal access tokens**

You'll see all active tokens, their scopes, and last-used date.

---

## 🎯 Quick Recap

| Step | Command / Action |
|---|---|
| 1. Create token | GitHub → Settings → Developer settings → Tokens (classic) |
| 2. Enable storage | `git config --global credential.helper store` |
| 3. Push once | `git push` → enter username + token |
| 4. Verify | `cat ~/.git-credentials` |
| 5. Secure file | `chmod 600 ~/.git-credentials` |
| 6. Revoke if leaked | GitHub → Settings → Developer settings → delete token |

---

**Done.** You've now set up GitHub authentication the proper way.
No more password errors, no more typing tokens every time. 🚀
### 📋 What This Covers

| Section | Purpose |
|---|---|
| Why a token? | Explains why GitHub stopped accepting passwords |
| Create token | Step-by-step with screenshots-style directions |
| Save token | One command to store it forever |
| Use token | What to type when prompted |
| Verify | Check the file exists and is correct |
| Secure | Set file permissions to `600` |
| Test | Push once to confirm it works |
| Troubleshoot | What to do if it fails, how to revoke |

# Code the Future </>

## Session 1: HTTPS vs SSH (optional)

### Content covered in this session

- The two ways to connect to GitHub: HTTPS and SSH
- Which one to use, and how to set up each

### Session goals

- Understand the difference between HTTPS and SSH
- Be able to clone, pull and push using **either** option

---

### Why is there a choice?

When you clone a repo and click the green **'Code'** button on GitHub, you'll see a few tabs - **HTTPS** and **SSH** (and others). These are just two different ways for your computer to talk to GitHub. They do the same job; they only differ in **how you prove who you are** when you push code.

The URL you copy tells Git which method to use:

<table style="color: white;">
  <thead>
    <tr>
      <th style="color: white; text-align: left;">Method</th>
      <th style="color: white; text-align: left;">The clone URL looks like...</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="color: white;">HTTPS</td>
      <td style="color: white;"><code>https://github.com/your-username/your-repo.git</code></td>
    </tr>
    <tr>
      <td style="color: white;">SSH</td>
      <td style="color: white;"><code>git@github.com:your-username/your-repo.git</code></td>
    </tr>
  </tbody>
</table>

**Important:** you must have set up the matching authentication *before* you push. If you copy an **SSH** URL but haven't created an SSH key, your first `git push` will fail with an error like `Permission denied (publickey)`. This is the most common reason people get stuck!

---

### Which should I use?

**If you're not sure, use HTTPS.** It works everywhere, needs the least setup, and is the recommended choice for this course.

SSH is a great option once you're comfortable - you set it up once and then never have to type a token again. Feel free to try it, but you don't need it to complete the course.

---

### Option 1: HTTPS (recommended for beginners)

1. On GitHub, click **'Code'**, choose the **HTTPS** tab, and copy the URL.
2. Clone as normal: `git clone https://github.com/your-username/your-repo.git`
3. The first time you `git push`, Git will ask you to sign in.

**Watch out:** GitHub no longer accepts your account **password** on the command line. When it asks for a password, you need a **Personal Access Token (PAT)** instead.

#### Creating a Personal Access Token (PAT)

1. On GitHub, click your profile picture (top right) -> **Settings**.
2. Scroll down to **Developer settings** (bottom of the left menu).
3. Go to **Personal access tokens -> Tokens (classic)** -> **Generate new token (classic)**.
4. Give it a name (e.g. "Code the Future laptop"), set an expiry, and tick the **`repo`** scope.
5. Click **Generate token** and **copy it now** - you won't be able to see it again.
6. When Git asks for your **password** on the command line, paste the **token** instead of your password.

Most computers will remember the token after the first time (via the built-in credential manager), so you usually only do this once.

---

### Option 2: SSH (set up once, no tokens needed)

SSH uses a pair of keys stored on your computer: a **private** key (which stays secret on your machine) and a **public** key (which you give to GitHub). GitHub matches them to confirm it's really you.

#### Step 1: Check for an existing key

```
ls -al ~/.ssh
```

If you see a file called `id_ed25519.pub` (or `id_rsa.pub`), you already have a key and can skip to Step 3.

#### Step 2: Generate a new key

```
ssh-keygen -t ed25519 -C "your_email@example.com"
```

Press **Enter** to accept the default file location. You can add a passphrase for extra security or press **Enter** to skip it.

#### Step 3: Copy your public key

**Mac:**

```
pbcopy < ~/.ssh/id_ed25519.pub
```

**Windows (Git Bash):**

```
cat ~/.ssh/id_ed25519.pub | clip
```

If those don't work, just open the `.pub` file in a text editor and copy everything inside it.

**Only ever share the `.pub` (public) file.** Never share the file *without* `.pub` - that's your private key and must stay secret.

#### Step 4: Add the key to GitHub

1. On GitHub, go to **Settings -> SSH and GPG keys**.
2. Click **New SSH key**.
3. Give it a title (e.g. "My laptop"), paste your public key into the box, and click **Add SSH key**.

#### Step 5: Test it

```
ssh -T git@github.com
```

If it works you'll see a message like:

```
Hi your-username! You've successfully authenticated...
```

Now clone using the **SSH** URL and push away - no token needed.

---

### Already cloned with the "wrong" one?

No need to re-clone. You can switch a repo between HTTPS and SSH at any time.

Check which one you're currently using:

```
git remote -v
```

Switch to SSH:

```
git remote set-url origin git@github.com:your-username/your-repo.git
```

Switch to HTTPS:

```
git remote set-url origin https://github.com/your-username/your-repo.git
```

---

### Resources

<ul>
<li><a href='https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens' target='_blank' title="GitHub Docs - Personal access tokens">GitHub Docs - Personal access tokens</a></li>
<li><a href='https://docs.github.com/en/authentication/connecting-to-github-with-ssh' target='_blank' title="GitHub Docs - Connecting with SSH">GitHub Docs - Connecting to GitHub with SSH</a></li>
<li><a href='https://docs.github.com/en/get-started/git-basics/about-remote-repositories' target='_blank' title="GitHub Docs - HTTPS vs SSH remotes">GitHub Docs - About remote repositories</a></li>
</ul>

<div style="width: 100%">
<a href='git_and_terminal.md'><-- Previous section: Git via Terminal</a>
<div align="right"><a  href='git_and_desktop.md'>Next section: Git via GitHub Desktop --></a></div>
</div>
</div>

![nosnap](https://socialify.git.ci/VincentZyu233/nosnap/image?description=1&font=Jost&forks=1&issues=1&language=1&logo=https%3A%2F%2Favatars.githubusercontent.com%2Fu%2F142771491%3Fv%3D4&name=1&owner=1&pulls=1&stargazers=1&theme=Auto)
# 🚫 NoSnap

> **Ubuntu, why are you so obsessed with Snap?**

One-click removal of the Snap ecosystem from Ubuntu, giving you back a clean Linux environment.

---

## 🤔 Why should I care?

Once upon a time, Ubuntu was everyone's first love for entering the Linux world — lightweight, elegant, works out of the box.

But at some point, Canonical decided to become the Snap salesperson of the year, cramming it into every orifice of your system:

- 🐌 **Impressively slow startup**: A calculator app takes 5 seconds to open. Are you running Windows 11 or something?
- 💽 **`/dev/loop` spam**: Run `lsblk` once and enjoy an endless list of loop devices. It's like counting sheep, except you're not trying to sleep.
- 🎃 **Disk space black hole**: Every Snap package bundles its own runtime. 500MB for a calculator? Ubuntu is really paying tribute to Windows' volumetric artistry.
- 🔒 **Forced auto-updates**: Where's your Linux freedom now? Did Canonical eat your user agency?
- 🧟 **The unkillable snapd**: You remove it. It comes back. More stubborn than a terminal rash.

Ubuntu gets fatter by the day. At this rate it's going to get excommunicated from the Linux community. Other distros are trimming the fat, and Ubuntu is over here force-feeding you proprietary garbage. `apt install chromium` gives you a Snap version — isn't that crying wolf while selling dog meat?

So, **NoSnap** was born. One script, one command, rip Snap out by the roots, never to return.

---

## ✨ Features

- ✅ Stop and disable all Snap-related services
- ✅ Uninstall all Snap packages in dependency order
- ✅ Completely purge the `snapd` package itself
- ✅ Clean up every Snap leftover (`~/snap`, `/var/lib/snapd`, etc.)
- ✅ Set APT pinning policy to **prevent `snapd` from ever crawling back**
- ✅ Show how much disk space you reclaimed — so you can bask in the sweet smell of freedom

---

## 🚀 Usage

### Method 1: One-liner (recommended)

```bash
# Run directly from GitHub
curl -fsSL https://raw.githubusercontent.com/VincentZyuApps/nosnap/main/nosnap.sh | sudo bash

# Or run directly from Gitee
curl -fsSL https://gitee.com/vincent-zyu/nosnap/raw/main/nosnap.sh | sudo bash
```

### Method 2: Clone locally

```bash
# Clone from GitHub
git clone https://github.com/VincentZyuApps/nosnap
# Or clone from Gitee
git clone https://gitee.com/vincent-zyu/nosnap
cd nosnap

# Make it executable
chmod +x nosnap.sh

# Run as root
sudo ./nosnap.sh
```

That's it. Faster than a coffee break, and Snap is gone from your system for good.

---

## ⚠️ Caveats

- Make sure you're running **Ubuntu / an Ubuntu-based distro** (Debian users generally don't have this problem — they're not being held hostage by Canonical).
- If you're using the Snap version of Firefox or other software, install an alternative via APT or a PPA before running the script. You've been warned.
- The script needs **root privileges**. We're performing surgery here, after all.

---

## 📋 What does the script actually do?

| Step | Action |
|------|--------|
| 1 | Calculate how much space Snap is wasting |
| 2 | Stop and disable `snapd`-related services |
| 3 | Uninstall all Snap packages one by one (regular first, then core) |
| 4 | `apt purge` to obliterate the `snapd` package |
| 5 | Delete all Snap residual directories |
| 6 | Apply APT pinning policy to permanently ban `snapd` installation |

---

## 🗣️ Final thoughts

The soul of Linux is **freedom and choice**. When a distro starts making decisions for you and shoving things nobody asked for down your throat, it's drifting away from the community.

Snap itself is not the sin. **Forced adoption is.**

Maybe one day Canonical will figure that out. Until then —

```
sudo ./nosnap.sh
```

---

---

## 🎙️ Community hot takes

There's a post on Zhihu asking: "What distro for Linux newcomers?"
The answer:
> First is Debian. Second is Ubuntu without Snap.

Translation: Debian is what Ubuntu wishes it could be. Ubuntu without Snap is just Debian in a trench coat, with a side of Canonical's questionable life choices.

The irony: the best Ubuntu is the one that least resembles Ubuntu. This is the "we have Debian at home" meme come to life.

---

## 📜 License

MIT — use it freely, the way Linux was always meant to be.

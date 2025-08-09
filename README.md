# Setting Up Oh My Posh with `quick-term` Theme in Git Bash

This guide walks you through the complete process of installing and configuring [Oh My Posh](https://ohmyposh.dev/) in **Git Bash** on Windows, using the **quick-term** theme. It also covers font setup for icons and making the theme load automatically.

---

## Prerequisites

- Git Bash installed on Windows
- Internet connection to download files
- Basic familiarity with terminal commands

---

## Step 1: Install Oh My Posh

Oh My Posh can be installed via several methods. The easiest on Windows is using [Scoop](https://scoop.sh/):

1. Open Git Bash.
2. Check if `scoop` is installed by running:

   ```bash
   scoop --version
   ```

3. If `scoop` is not installed, install it by running in **PowerShell (not Git Bash)**:

   ```powershell
   iwr -useb get.scoop.sh | iex
   ```

4. Once `scoop` is ready, install Oh My Posh:

   ```bash
   scoop install oh-my-posh
   ```

Alternatively, download the latest release binary from the [Oh My Posh Releases](https://github.com/JanDeDobbeleer/oh-my-posh/releases) page and add it to your system `PATH`.

---

## Step 2: Download the `quick-term` Theme

1. Create a folder to store Oh My Posh themes:

   ```bash
   mkdir -p ~/.poshthemes
   ```

2. Download the `quick-term` theme JSON file:

   ```bash
   curl -Lo ~/.poshthemes/quick-term.omp.json https://raw.githubusercontent.com/JanDeDobbeleer/oh-my-posh/main/themes/quick-term.omp.json
   ```

---

## Step 3: Set Git Bash Font to a Nerd Font

Oh My Posh uses icons that require Nerd Fonts to display properly.

1. Download a Nerd Font such as [JetBrainsMono Nerd Font](https://www.nerdfonts.com/font-downloads).
2. Install the font on your Windows system by double-clicking the downloaded `.ttf` file and clicking **Install**.
3. Open Git Bash.
4. Right-click the **Git Bash window title bar**, then select **Options...**.
5. In the **Options** window, go to the **Text** tab.
6. Under **Font**, select your installed Nerd Font (e.g., *JetBrainsMono Nerd Font*).
7. Click **OK** and restart Git Bash.

---

## Step 4: Configure Git Bash to Load Oh My Posh Theme Automatically

1. Open your `.bashrc` file in a text editor. For example, using nano:

   ```bash
   nano ~/.bashrc
   ```

2. Add the following line at the end of the file:

   ```bash
   eval "$(oh-my-posh init bash --config ~/.poshthemes/quick-term.omp.json)"
   ```

3. Save and exit the editor:
   - Press `Ctrl + O`, then `Enter` to save.
   - Press `Ctrl + X` to exit nano.

---

## Step 5: Reload Your Shell

To apply the changes immediately without restarting Git Bash, run:

```bash
source ~/.bashrc
```

Alternatively, close and reopen Git Bash.

---

## Step 6: Verify the New Prompt

Your terminal prompt should now display the **quick-term** Oh My Posh theme with icons and colors.

---

## Troubleshooting Tips

- **Icons not showing correctly:** Ensure your terminal font is set to a Nerd Font.
- **Theme not loading:** Verify the path to the theme file is correct and the theme file exists.
- **Command not found:** Confirm Oh My Posh is installed and accessible in your system `PATH`.

---

## Additional Resources

- [Oh My Posh Documentation](https://ohmyposh.dev/docs/)
- [Nerd Fonts](https://www.nerdfonts.com/)
- [Git Bash Download](https://git-scm.com/downloads)
- [Scoop - Windows Package Manager](https://scoop.sh/)

---

If you want help customizing your theme or adding new features, feel free to ask!

```
    _   __      __  _                _____                        __          __
   / | / /___  / /_(_)___  ____     / ___/____  ____ _____  _____/ /_  ____  / /_
  /  |/ / __ \/ __/ / __ \/ __ \    \__ \/ __ \/ __ `/ __ \/ ___/ __ \/ __ \/ __/
 / /|  / /_/ / /_/ / /_/ / / / /   ___/ / / / / /_/ / /_/ (__  ) / / / /_/ / /_
/_/ |_/\____/\__/_/\____/_/ /_/   /____/_/ /_/\__,_/ .___/____/_/ /_/\____/\__/
                                                    /_/

Back up your data – free yourself from the Notion lock-in.
```

Notion's default HTML export lacks style (and even content), while our files retain the original page's appearance and remove unnecessary JavaScript resulting in smaller file sizes and faster load times.

| <img width="685" src="docs/assets/export.jpeg"> | <img width="685" src="docs/assets/snapshot.jpeg"> | <img width="685" src="docs/assets/original.jpeg"> |
| :---------------------------------------------: | :-----------------------------------------------: | :-----------------------------------------------: |
|                 Default export                  |              **✨NotionSnapshot✨**               |                   Original page                   |

<br><br><br><br>

# Installation

First you must set the page that you want to export to be publicly accessible:

1. Open the page you want to export to HTML in Notion
2. Click on the `Publish` tab
3. Click on the `Publish to web` button
4. Copy the link to the page by clicking on the `Copy web link` button

Make sure to store the link you just copied somewhere you will find again later.

<br>

### 1. Installing dependencies

First install the following dependencies:

-   [WSL (Windows Subsystem for Linux)](https://learn.microsoft.com/en-us/windows/wsl/install) if you are on a Windows machine, as this tool is developed for Unix
-   [Python 3](https://www.python.org/downloads/)
-   [Chrome](https://www.google.com/chrome/)

Installing Chrome on WSL/Ubuntu can be a little bit tricky, but here is what worked for me:

```bash
sudo apt update && sudo apt upgrade -y
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo dpkg -i google-chrome-stable_current_amd64.deb
sudo apt --fix-broken install
rm -rf google-chrome-stable_current_amd64.deb
```

<br>

### 2. Cloning the repository

Next clone this repository:

```bash
git clone https://github.com/sueszli/notionSnapshot.git
cd notionSnapshot
```

<br>

### 3. Running the application

Finally run the application.

Use the `-h` or `--help` flag when running the script to see all the options that are available:

```bash
python3 notionsnapshot --help
```

You can for instance scrape the pages in dark mode by using the `--dark-mode` option or display the browser while scraping by using the `--show-browser` option.

Once you've made up your mind, you can run the script with the URL of the Notion page you want to scrape:

```bash
python3 notionsnapshot <notion page url>
```

Alternatively you can run some of our test pages which are listed in the `test.sh` file.

<br><br><br><br>

---

Special thanks to:

-   Leonardo Cavaletti who laid the foundation of this project with his lovely loconotion project
-   [MJDeligan](https://github.com/MJDeligan) the main contributor, who resolved the hardest issues and added the most important features

aswell as Stefan Brandmair, Thomas Biedermann and Berndt Uhlig who helped me with the initial setup of this project.

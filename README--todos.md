# Todos

- [cheat sheet](#linux-command-line-cheat-sheet)
- [twig videos](#twig-videos)
- [setup custom theme (bootstrap 5)](#setup-custom-theme-bootstrap-5)

---

## Linux command line cheat sheet

A working set of Linux commands for this course: navigating the filesystem, editing files, Git, Sass, and Drupal theme work.

### Getting help

```bash
command --help          # short usage for most commands
man command             # full manual (q to quit)
whatis command          # one-line description
which command           # where the program lives
type command            # alias, builtin, or file
history                 # list recent commands
!!                      # repeat last command
!$                      # last argument of previous command
```

### Navigation and filesystem

```bash
pwd                     # print working directory
ls                      # list files
ls -la                  # long list, including hidden files
ls -lh                  # human-readable sizes
cd /path/to/dir         # change directory
cd ~                    # home directory
cd -                    # previous directory
cd ..                   # parent directory
mkdir project           # create a directory
mkdir -p themes/custom/mytheme/css
touch file.txt          # create an empty file
cp file.txt backup.txt  # copy a file
cp -r src dest          # copy a directory
mv old.txt new.txt      # rename or move
rm file.txt             # delete a file
rm -r dirname           # delete a directory
rm -rf dirname          # delete without prompts (use carefully)
find . -name "*.twig"   # find files by name
find . -type d          # find directories
tree                    # show directory tree (if installed)
```

### Viewing and editing files

```bash
cat file.txt            # print entire file
less file.txt           # page through a file (q to quit)
head -n 20 file.txt     # first 20 lines
tail -n 20 file.txt     # last 20 lines
tail -f error.log       # follow a log as it grows
nano file.txt           # simple editor
code .                  # open current folder in VS Code / Cursor
wc -l file.txt          # count lines
diff a.txt b.txt        # compare two files
```

### Searching text

```bash
grep "navbar" *.css
grep -R "base theme" themes/
grep -n "container" templates/page.html.twig
grep -i error *.log     # case-insensitive
grep -v "comment" file  # invert match (exclude)
```

### Permissions and ownership

```bash
ls -l                   # see permissions
chmod 644 file.css      # rw-r--r--
chmod 755 script.sh     # rwxr-xr-x
chmod +x script.sh      # make executable
chown user:group file
sudo command            # run as administrator
whoami                  # current user
id                      # user and group ids
```

Linux permission bits: `r` = 4, `w` = 2, `x` = 1. Example: `7` = rwx, `6` = rw-, `5` = r-x.

### Processes, disk, and environment

```bash
ps aux                  # running processes
top                     # live process monitor
htop                    # nicer process monitor (if installed)
kill PID                # stop a process
kill -9 PID             # force stop
df -h                   # disk space
du -sh *                # size of each item in the current directory
free -h                 # memory
uname -a                # kernel / OS info
echo $PATH              # executable search path
export VAR=value        # set an environment variable
env                     # list environment variables
clear                   # clear the terminal
```

### Archives and download

```bash
tar -czvf archive.tar.gz folder/
tar -xzvf archive.tar.gz
zip -r archive.zip folder/
unzip archive.zip
curl -O https://example.com/file.css
wget https://example.com/file.css
```

### Networking and SSH

```bash
ping example.com
ip addr                 # network interfaces (modern)
ifconfig                # network interfaces (older)
ss -tuln                # listening ports
curl -I https://example.com
ssh user@host
scp file.txt user@host:/path/
```

### Package managers

Debian / Ubuntu / WSL (apt):

```bash
sudo apt update
sudo apt upgrade
sudo apt install git sass nodejs npm
sudo apt remove package
apt search keyword
```

Fedora:

```bash
sudo dnf install git
```

macOS (Homebrew, if used alongside Linux notes):

```bash
brew install sass/sass/sass
```

### Users, pipes, and redirection

```bash
command > file.txt      # overwrite stdout into a file
command >> file.txt     # append stdout
command 2> errors.log   # redirect errors
command | grep error    # pipe output into another command
command1 && command2    # run second only if first succeeds
command1 || command2    # run second only if first fails
```

### Git (command line)

```bash
git status
git add .
git add path/to/file
git commit -m "Describe why the change was made"
git log --oneline
git diff
git branch
git checkout -b feature-name
git pull
git push
git clone https://github.com/user/repo.git
```

### Sass compilation

```bash
sass --version
sass scss/style.scss css/style.css
sass --watch scss/style.scss css/style.css
sass scss/style.scss css/style.css && sass scss/ck5style.scss css/ck5style.css
```

### Drupal / Drush / DDEV (theme work)

```bash
# DDEV
ddev start
ddev drush cr                       # rebuild caches
ddev drush theme:enable mytheme
ddev drush config:set system.theme default mytheme -y
ddev ssh                            # shell inside the container
ddev npx sass --quiet scss/style.scss css/style.css

# Drush on a local Drupal site
drush cr
drush status
drush theme:list
drush theme:enable bootstrap5
drush theme:enable mytheme
drush config:set system.theme default mytheme -y
drush watchdog:show --count=10
```

### Useful path shortcuts

```bash
~          home directory
.          current directory
..         parent directory
*          any characters
*.twig     all Twig files in this folder
```

### Typical workflow for this course

```bash
cd ~/project
pwd
ls -la
mkdir -p themes/custom/mytheme/{css,scss,js,templates}
cd themes/custom/mytheme
nano mytheme.info.yml
sass --watch scss/style.scss css/style.css
git status
git add .
git commit -m "Add Bootstrap 5 subtheme files"
```

---

## Twig videos

Five YouTube videos that explain what Twig is and how to write Twig templates. Watch in this order.

1. **[Twig Template Engine for PHP: Introduction](https://www.youtube.com/watch?v=KB1jTDJweLY)** — Jeremy McPeak. What Twig is, why templates exist, and the core ideas: print syntax, blocks, inheritance, and auto-escaping.
2. **[PHP Templating with Twig: Installing (Part 1/5)](https://www.youtube.com/watch?v=SVb0whlghQY)** — How Twig is installed and wired into a PHP project so templates can be rendered.
3. **[PHP Templating with Twig: Customising Syntax (Part 4/5)](https://www.youtube.com/watch?v=8Oay6RPMF9M)** — How Twig tags, delimiters, and template syntax work when you write actual template code.
4. **[How to set up a Twig template file and a brief description of Twig variables](https://www.youtube.com/watch?v=8yrF79A0jYE)** — Drupal-focused: creating an `.html.twig` file, printing variables with `{{ }}`, and why markup belongs in templates instead of PHP.
5. **[Getting Started with Twig Templates in Drupal CMS](https://www.youtube.com/watch?v=St-OKBxYuao)** — How Drupal maps render variables into Twig templates and how to print them on a page.

Optional extra after those five: [Creating Custom Twig Template to Display View Data in Drupal](https://www.youtube.com/watch?v=7jqoy7R1dzs) (Drupal Academy) — overriding a Views Twig template and printing individual fields.

Quick Twig syntax reminder while watching:

```twig
{# comment #}
{{ variable }}
{{ variable|escape }}
{% if page.header %}
  {{ page.header }}
{% endif %}
{% for item in items %}
  <li>{{ item.title }}</li>
{% endfor %}
```

---

## Setup custom theme (Bootstrap 5)

This is how to create a **Drupal custom subtheme** that uses the contributed **Bootstrap5** base theme (`drupal/bootstrap5`). Do not customize the base theme itself. Put overrides in the subtheme so Bootstrap upgrades stay possible.

The examples below use:

- Drupal 10 or 11
- Base theme: `bootstrap5`
- Subtheme machine name: `mytheme`
- Human name: `My Theme`

### 1. Install the Bootstrap5 base theme

From the Drupal project root (Composer layout):

```bash
composer require drupal/bootstrap5
drush theme:enable bootstrap5
drush cr
```

Or in the admin UI: **Appearance → Install Bootstrap5**. You can use Bootstrap5 as-is, but **template and CSS overrides belong in a subtheme**.

### 2. Generate the subtheme

**Option A — admin UI (easiest)**

1. Enable Bootstrap5.
2. Open `/admin/appearance/settings/bootstrap5`.
3. Scroll to **Subtheme**.
4. Enter a name (for example `My Theme`) and create it.
5. Drupal writes the theme under `web/themes/custom/`.

**Option B — Drush generator**

```bash
drush --include="web/themes/contrib/bootstrap5/src/Drush" \
  bootstrap5:generate-subtheme mytheme \
  --subtheme-name="My Theme"
```

**Option C — create the files by hand** (below). Use this if the generator is unavailable, or to understand every file.

### 3. Target folder structure

```text
web/themes/custom/mytheme/
├── mytheme.info.yml
├── mytheme.libraries.yml
├── mytheme.theme
├── screenshot.png
├── config/
│   ├── install/
│   │   └── mytheme.settings.yml
│   └── schema/
│       └── mytheme.schema.yml
├── css/
│   ├── style.css
│   └── ck5style.css
├── scss/
│   ├── _variables_bootstrap.scss
│   ├── _variables_drupal.scss
│   ├── style.scss
│   └── ck5style.scss
├── js/
│   └── custom.js
└── templates/
    ├── layout/
    │   └── page.html.twig
    └── node/
        └── node.html.twig
```

Create it:

```bash
mkdir -p web/themes/custom/mytheme/{css,scss,js,templates/layout,templates/node,config/install,config/schema}
cd web/themes/custom/mytheme
```

### 4. `mytheme.info.yml` — declare the subtheme

```yaml
name: My Theme
type: theme
description: 'Custom Bootstrap 5 subtheme for the course website.'
core_version_requirement: ^10 || ^11
base theme: bootstrap5
starterkit: false

libraries:
  - mytheme/global-styling

libraries-extend:
  bootstrap5/global-styling:
    - mytheme/global-styling

regions:
  header: Header
  nav_branding: 'Navigation branding'
  nav_main: 'Main navigation'
  nav_additional: 'Additional navigation'
  breadcrumb: Breadcrumbs
  content: Content
  sidebar_first: 'First sidebar'
  sidebar_second: 'Second sidebar'
  footer: Footer

# Match Bootstrap 5 breakpoints used by the base theme.
breakpoints: bootstrap5.breakpoints.yml
```

Notes:

- `base theme: bootstrap5` is what makes this a subtheme. Do not set `base theme: false` if you want Bootstrap5 templates, regions, and libraries.
- `libraries` attaches your CSS/JS on every page of this theme.
- Region names must match what you print in `page.html.twig`. If you generate the subtheme from the UI, keep the regions it creates unless you also update the page template.

### 5. `mytheme.libraries.yml` — register CSS and JS

```yaml
global-styling:
  version: VERSION
  css:
    theme:
      css/style.css: {}
  js:
    js/custom.js: {}
  dependencies:
    - core/drupal
    - bootstrap5/bootstrap5
```

CKEditor 5 preview styles (so the admin editor matches the frontend):

```yaml
ckeditor5:
  css:
    theme:
      css/ck5style.css: {}
```

Then in `mytheme.info.yml`:

```yaml
ckeditor5-stylesheets:
  - css/ck5style.css
```

Drupal only loads files that are defined as libraries and then attached. Putting a CSS file in the folder is not enough.

### 6. Override Bootstrap and Drupal Sass variables

Edit **copies in the subtheme**, not the files inside `themes/contrib/bootstrap5`.

`scss/_variables_bootstrap.scss`:

```scss
// Override Bootstrap 5 variables BEFORE Bootstrap is imported.
// Source of names: themes/contrib/bootstrap5/dist/bootstrap/5.3.x/scss/_variables.scss

$primary: #003366;
$secondary: #e7b645;
$font-family-sans-serif: "Segoe UI", system-ui, sans-serif;
$font-size-base: 1.05rem;
$border-radius: 0.5rem;
$enable-shadows: true;

// Optional: add a custom brand color to Bootstrap's map.
$custom-colors: (
  "brand": #003366
);
$theme-colors: map-merge($theme-colors, $custom-colors);
```

If `$theme-colors` is not defined yet when this file is loaded, skip the `map-merge` block and only set `$primary` / `$secondary`. The generated Bootstrap5 subtheme already imports files in the correct order.

`scss/_variables_drupal.scss`:

```scss
// Drupal-specific Bootstrap5 theme variables.
$navbar-brand-site-title-text-transform: none;
$navbar-brand-site-title-font-size: 1.25rem;
$navbar-brand-site-title-letter-spacing: 0;
$footer-padding: 2rem 0;
$region-padding: 0;
```

`scss/style.scss` (typical generated import order):

```scss
// 1. Variable overrides
@import "variables_bootstrap";
@import "variables_drupal";

// 2. Parent Bootstrap 5 + Drupal styles
@import "../../contrib/bootstrap5/scss/style";

// 3. Custom component CSS
.site-header {
  background-color: $primary;
  color: #fff;
}

.btn-primary {
  text-transform: none;
}

.region-footer {
  background-color: $primary;
  color: #fff;
}
```

If the generator already created `style.scss`, keep its `@import` paths and only add your rules at the bottom.

Compile:

```bash
cd web/themes/custom/mytheme
sass scss/style.scss css/style.css
sass scss/ck5style.scss css/ck5style.css

# watch while developing
sass --watch scss/style.scss:css/style.css scss/ck5style.scss:css/ck5style.css
```

With DDEV:

```bash
ddev npx sass --quiet scss/style.scss css/style.css
```

Never edit compiled `css/style.css` by hand if you are using Sass. Change SCSS, then recompile.

### 7. `mytheme.theme` — preprocess and extra libraries

```php
<?php

/**
 * @file
 * Functions to support theming in the My Theme subtheme.
 */

/**
 * Implements hook_preprocess_HOOK() for page.
 */
function mytheme_preprocess_page(array &$variables) {
  $variables['site_branding'] = [
    'name' => \Drupal::config('system.site')->get('name'),
  ];
}

/**
 * Implements hook_form_system_theme_settings_alter().
 */
function mytheme_form_system_theme_settings_alter(&$form, \Drupal\Core\Form\FormStateInterface $form_state) {
  $form['mytheme_settings'] = [
    '#type' => 'details',
    '#title' => t('My Theme settings'),
    '#open' => TRUE,
  ];

  $form['mytheme_settings']['show_credit'] = [
    '#type' => 'checkbox',
    '#title' => t('Show footer credit'),
    '#default_value' => theme_get_setting('show_credit'),
  ];
}
```

Every PHP function must use the **machine name prefix** `mytheme_`. If you rename the theme, rename these functions too.

### 8. Override Twig templates

Copy a template from the base theme (or core) into the subtheme **using the same filename**. Drupal then uses your copy.

```bash
cp web/themes/contrib/bootstrap5/templates/layout/page.html.twig \
   web/themes/custom/mytheme/templates/layout/page.html.twig
```

Example `templates/layout/page.html.twig` using Bootstrap 5 layout classes:

```twig
<div class="site-wrapper">
  <header class="site-header navbar navbar-expand-lg navbar-dark bg-primary">
    <div class="container">
      {{ page.nav_branding }}
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#mainNav">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="mainNav">
        {{ page.nav_main }}
        {{ page.nav_additional }}
      </div>
    </div>
  </header>

  {% if page.breadcrumb %}
    <div class="container py-2">
      {{ page.breadcrumb }}
    </div>
  {% endif %}

  <main class="container my-4">
    <div class="row">
      {% if page.sidebar_first %}
        <aside class="col-lg-3 mb-4">
          {{ page.sidebar_first }}
        </aside>
      {% endif %}

      <section class="{{ page.sidebar_first or page.sidebar_second ? 'col-lg-6' : 'col-12' }}">
        {{ page.content }}
      </section>

      {% if page.sidebar_second %}
        <aside class="col-lg-3 mb-4">
          {{ page.sidebar_second }}
        </aside>
      {% endif %}
    </div>
  </main>

  <footer class="region-footer bg-primary text-white py-4">
    <div class="container">
      {{ page.footer }}
    </div>
  </footer>
</div>
```

Example node template `templates/node/node.html.twig`:

```twig
<article{{ attributes.addClass('card', 'mb-4', 'shadow-sm') }}>
  <div class="card-body">
    {{ title_prefix }}
    {% if not page %}
      <h2{{ title_attributes.addClass('card-title') }}>
        <a href="{{ url }}" rel="bookmark">{{ label }}</a>
      </h2>
    {% endif %}
    {{ title_suffix }}

    {% if display_submitted %}
      <div class="card-subtitle mb-2 text-muted">
        {{ author_picture }}
        {{ submitted }}
      </div>
    {% endif %}

    <div{{ content_attributes.addClass('card-text') }}>
      {{ content }}
    </div>
  </div>
</article>
```

After any template change:

```bash
drush cr
```

Turn on Twig debug while developing (`sites/default/services.yml`):

```yaml
parameters:
  twig.config:
    debug: true
    auto_reload: true
    cache: false
```

Then rebuild caches. HTML comments will show which Twig file Drupal used and suggested override names.

### 9. Enable the subtheme and set it as default

```bash
drush theme:enable mytheme
drush config:set system.theme default mytheme -y
drush cr
```

Or: **Appearance → Install My Theme → Set as default**.

Place blocks into the new regions at **Structure → Block layout** after you switch themes. Regions from the old theme do not automatically remap.

### 10. Verify the setup

1. Visit the site as an anonymous user and confirm Bootstrap grid, navbar, and buttons still work.
2. Confirm your `$primary` color appears on `.btn-primary` and the header after Sass compile + cache rebuild.
3. Confirm custom CSS in `css/style.css` is present in the page source as `mytheme/css/style.css`.
4. Confirm `page.html.twig` from `themes/custom/mytheme` is the template listed in Twig debug comments.
5. Do **not** put overrides in `themes/contrib/bootstrap5`. If you did, move them into the subtheme.

### Common mistakes

| Problem | Cause | Fix |
| --- | --- | --- |
| Theme does not appear | Wrong folder (`modules/` or `themes/contrib/`) or invalid YAML | Put it in `themes/custom/mytheme/` and validate `.info.yml` |
| Styles missing | Library not defined or not attached | Add `mytheme/global-styling` to `libraries:` |
| Bootstrap looks unstyled | Base theme not installed / not `bootstrap5` | Enable `bootstrap5` and set `base theme: bootstrap5` |
| SCSS changes do nothing | CSS not recompiled, or you edited `css/style.css` while Sass overwrites it | Re-run `sass` and `drush cr` |
| Twig changes do nothing | Render cache | `drush cr` and enable Twig auto-reload |
| PHP error in `.theme` | Function name does not match machine name | Use `mytheme_preprocess_page`, not `my_theme_...` |
| Regions empty | `page.html.twig` prints a region not listed in `.info.yml` | Keep region keys identical in both files |

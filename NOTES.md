# Linomath notes


## 2023-11-15

### Python implementation of ed editor

#### Prior Python ed

1. <https://pypi.org/search/?q=python+ed+editor>.
2. <https://pypi.org/project/ed/>.
3. <https://github.com/eumiro/ed/>.

Item 3 implements a buffer object.

1. <https://github.com/topics/ed?l=python>.
2. <https://github.com/linarphy/py_ed>.
3. <https://github.com/That1M8Head/Streakline>.

Item 1 gives 11 repositories including the previous eumiro. Items 2
and 3 are only items of interest in search 1.

Item 2 gives a single 800 line Python file, much of which is devoted
to command line options. State, such as current and last command,
stored as global variables.

Item 3 is abandoned.

#### Prior Python readline

The `ed` command uses GNU `readline` if available, as does the Python
REPL on Linux. But `readline` is not available on Windows.

1. <https://www.google.com/search?q=readline+windows>.
2. <https://gnuwin32.sourceforge.net/packages/readline.htm>.
3. <https://stackoverflow.com/questions/51157443/pythons-readline-module-not-available-for-windows>.
4. <https://tiswww.case.edu/php/chet/readline/rltop.html>.
5. <https://bugs.python.org/issue45870>.
6. <https://en.wikipedia.org/wiki/GNU_Readline>.
7. <https://pypi.org/project/readline/>.
8. <https://copdips.com/2018/05/using-readline-in-python-repl-on-windows.html>
9. <https://readthedocs.org/projects/windows-readline/>.
10. <https://github.com/PowerShell/PSReadLine>.
11. <https://github.com/JuliaAttic/readline>.

Item 2 is stale. Last changed 2008.

Item 3 suggests instead of `pyreadline` use
12. <https://github.com/pyreadline3/pyreadline3>.

Item 5 has been migrated to github. Closed in 2022 due to lack of
interest in submitting a docs pull request documenting pyreadline3.
13. <https://github.com/python/cpython/issues/90028>

Item 8 references IPython, which replaced `PyReadline` by
14. <https://python-prompt-toolkit.readthedocs.io/en/stable/>

### Aria speech in Firefox

I started this topic hoping to find a work around for Orca not working
for me on Sway / Wayland. I naively thought that it was enough to
provide Aria attributes, and then Firefox would do the rest. However,
Aria requires a screen reader to be present.

My misunderstanding is well summed up by the search, whose results
disappointed me until I understood what was going on.

- <https://www.google.com/search?q=firefox+enable+aria>.

#### Screen reader emulator

1. <https://www.google.com/search?q=screen+reader+emulator>.
2. <https://silktide.com/tools/toolbar/>.
3. <https://webaim.org/simulations/screenreader>.
4. <https://stackoverflow.com/questions/43340690/is-there-an-online-emulating-screen-reader-tool-to-test-against-a-custom-web-pag>.
5. <https://etc.usf.edu/techease/4all/web-accessibility/using-the-fangs-screen-reader-emulator/>.
6. <https://assistivlabs.com/use-cases/online-screen-reader-testing>
7. <https://www.standards-schmandards.com/projects/fangs.html>.

#### Chrome Vox

Somehow I was led to Chrome Vox, which I had heard of.

1. <https://www.google.com/search?q=chrome+vox>.
2. <https://chromewebstore.google.com/detail/screen-reader/kgejglhpjiefppelpmljglcjbhoiplfn>
3. <https://www.lenovo.com/us/en/glossary/chromevox/>.
4. <https://support.google.com/chromebook/answer/7031755?hl=en-GB>.
5. <https://pressbooks.library.torontomu.ca/wafd/chapter/chromevox-screen-reader-install-and-setup/>.
6. <https://hikeorders.com/accessibility/glossary/what-is-chrome-vox/>.
7. <https://www.unimelb.edu.au/accessibility/tools/screen-reader-testing>.

I tried Chrome Vox on Linux and found no voices shown in Options. So
game over. The reviews (perhaps on other platforms) were terrible.

- <chrome-extension://kgejglhpjiefppelpmljglcjbhoiplfn/chromevox/background/options.html>.
- <https://chrome.google.com/webstore/detail/screen-reader/kgejglhpjiefppelpmljglcjbhoiplfn>.


## 2023-11-13

### Orca screen reader

#### Orca links

I start with a search for `orca screen reader`.

1. <https://www.google.com/search?q=orca+screen+reader>.
2. <https://help.gnome.org/users/orca/stable/index.html.en>.
3. <https://en.wikipedia.org/wiki/Orca_(assistive_technology)>.
4. <https://help.gnome.org/users/orca/stable/introduction.html.en>.
5. <https://www.boia.org/blog/orca-screen-reader-an-overview-for-developers-and-content-creators>.
6. <https://www.a11yproject.com/posts/getting-started-with-orca/>.
7. <https://docs.oracle.com/cd/E26502_01/html/E29026/ats-2.html>.
8. <https://help.ubuntu.com/stable/ubuntu-help/a11y-screen-reader.html.en>.
9. <https://a11ysupport.io/learn/at/orca>.
10. <https://wiki.mozilla.org/Screen_Reader_-_Orca>.

#### Install Orca links

None of the above explain how to install Orca. So I for `install orca
screenreader`.

1. <https://www.google.com/search?q=install+orca+screen+reader>.
2. <https://wiki.debian.org/Accessibility/Orca>.
3. Link 6 above.
4. Link 8 above.
5. 404! <https://www.unixmen.com/install-screen-reader-orca-3-17-3-in-ubuntu-linux/>.
6. Link 4 above.
7. <https://techblog.wikimedia.org/2020/07/02/an-orca-screen-reader-tutorial/>.
8. <https://docs.fedoraproject.org/en-US/quick-docs/accessibility-post-installation-with-orca/>
9. <https://docs.oracle.com/en/operating-systems/oracle-linux/6/accessibility/ol-assistive-orca.html>.
10. <https://steamcommunity.com/groups/steamuniverse/discussions/1/6620895347254103056/>.
11. <https://www.kicksecure.com/wiki/Orca>.

For install I will use links 2, 7, 11.

#### Install Orca overview

Here's those links again.

2. <https://wiki.debian.org/Accessibility/Orca>.
7. <https://techblog.wikimedia.org/2020/07/02/an-orca-screen-reader-tutorial/>.
11. <https://www.kicksecure.com/wiki/Orca>.

Debian tells me to `sudo apt install orca`, and perhaps enable
autostart orca. For browsers it recommends firefox-esr. WebKit
considered not production ready.

Debian tells me that Orca uses speech-dispatcher to access speech
synthesizer. That's part of another documentation page:
- <https://wiki.debian.org/accessibility#Speech-Dispatcher>

Techblog says install `orca` and `espeak-ng`.

> The `espeak-ng` voices aren’t great at all, but so far they seem to
be the only thing that works.

Techblog provides a link to a YouTube video tutorial (from 2015,
12,000 view by 2023).  -
<https://www.youtube.com/watch?v=ieo20UtUobw>.

The Kicksecure page is interesting because it relates to virtual
machines. They suggest:
- `sudo apt install --no-install-recommends orca`

#### Install Orca

1. `sudo dnf update`.
2. `sudo dnf install orca`.
```
Installed:
  brlapi-0.8.4-10.fc38.x86_64           brltty-6.5-10.fc38.x86_64
  orca-44.1-1.fc38.noarch               pcre2-utf32-10.42-1.fc38.1.x86_64
  python3-brlapi-0.8.4-10.fc38.x86_64   python3-louis-3.25.0-1.fc38.noarch
  python3-pyatspi-2.46.0-2.fc38.noarch  python3-speechd-0.11.5-1.fc38.x86_64
```

Let's take a look.
```
orca --help
Usage: orca [-h] [-v] [-r] [-s] [-l] [-e OPTION] [-d OPTION] [-p NAME]
            [-u DIR] [--debug-file FILE] [--debug]

Optional arguments:
  -h, --help                   Show this help message and exit
  -v, --version                Version of this application
  -r, --replace                Replace a currently running instance of this
                               screen reader
  -s, --setup                  Set up user preferences (GUI version)
  -l, --list-apps              Print the known running applications
  -e OPTION, --enable OPTION   Force use of option
  -d OPTION, --disable OPTION  Prevent use of option
  -p NAME, --profile NAME      Load profile
  -u DIR, --user-prefs DIR     Use alternate directory for user preferences
  --debug-file FILE            Send debug output to the specified file
  --debug                      Send debug output to debug-YYYY-MM-DD-
                               HH:MM:SS.out

Report bugs to orca-list@gnome.org.
```

OK. So

1. First check my PC is connected to my stereo.
2. Start orca
```
$ orca -r
Warning:          Could not load keyboard geometry for :0
                  BadName (named color or font does not exist)
                  Resulting keymap file will not describe geometry

12:36:25.554207 - EVENT MANAGER: No focus
12:45:35.488892 - EVENT MANAGER: No focus
12:53:36.301321 - EVENT MANAGER: No focus
12:53:55.559620 - EVENT MANAGER: No focus
12:54:14.644890 - EVENT MANAGER: No focus
```
3. Ctrl-C does stop orca, but not immediately.

#### Orca and Sway

The warning about `geometry for :0` suggests a wayland problem. (I'm
using Sway.)

1. <https://www.google.com/search?q=orca+sway>.
2. <https://www.freelists.org/post/orca/Sway-window-manager-and-orca,5>.

The freelists/orca post is helpful with technical detail. It suggests
that if xwayland doesn't work then it won't be easy to fix. It's good
to know that this discussion, and the list it is on, both exist.

#### Freelists Orca

The Freelists Orca list is now an official Orca community tool,
replacing the GNOME hosted list. The move took place in November 2022.

1. <https://www.freelists.org/list/orca>.
2. <https://wiki.gnome.org/action/show/Projects/Orca>.
3. <https://mail.gnome.org/archives/orca-list/>.


#### Why Freelists Orca?

Briefly, in 2022 GNOME decided to migrate away from Mailman, and onto
Discourse. The Orca users weren't happy, and decided instead to
migrate to Freelists. More information in:

1. <https://mail.gnome.org/archives/orca-list/2022-September/thread.html>.
2. <https://mail.gnome.org/archives/orca-list/2022-October/thread.html>.
3. <https://mail.gnome.org/archives/orca-list/2022-November/thread.html>.

#### The Orca debug log

Running `orca -r --debug` and get many error. These include, every few
minutes:
```
Traceback (most recent call last):
  File "/usr/lib/python3.11/site-packages/orca/braille.py", line 1879, in init
    _brlAPI = brlapi.Connection()
              ^^^^^^^^^^^^^^^^^^^
  File "brlapi.pyx", line 456, in brlapi.Connection.__init__
brlapi.ConnectionError: couldn't connect to b':0' with key b'keyfile:/etc/brlapi.key+polkit': connect: No such file or directory
(brlerrno 11, libcerrno 2, gaierrno 0)
Is BRLTTY really running?
```

## 2023-11-08

### livereload

1. Search <https://www.google.com/search?q=livereload>.
2. It is a client-server protocol that reloads a web page whenever
relevant source changes.
3. The most canonical URL seems to be <https://github.com/livereload>.
4. It seems that there's no wikipedia page.
5. For Python livereload see <https://livereload.readthedocs.io/>.

### Software using livereload

I already knew that the following used livereload:
- Hugo: <https://gohugo.io/>
- MkDocs: <https://www.mkdocs.org/>
- Quarto: <https://quarto.org/>

### Installing Python livereload

Pip can do the installation: `pip install livereload`.

### Create workspace

1. Create an example directory: `mkdir example`.
2. Create two terminals on the example directory.
3. One terminal is for the server. The other is for the editor.

### View a livereload web page

You'll need a page to view, and a server to provide the live
reload. We'll do both in the server terminal.

1. Download this example HTML file:
> `wget https://raw.githubusercontent.com/lepture/python-livereload/master/example/index.html`
2. Run `livereload`. You'll get a lot of output, something like:
```
[I 231108 12:59:20 server:335] Serving on http://127.0.0.1:35729
[I 231108 12:59:20 handlers:62] Start watching changes
[I 231108 12:59:20 handlers:64] Start detecting changes
```

### View the livereload page

1. In a web brower, open the suggested link <http://127.0.0.1:35729>.
2. Refresh the web page. You'll see activity in the server terminal.

### Change the HTML file

1. In the editor window open an editor on the html file, say like so
> `$EDITOR index.html`.
2. Change the body of the HTML file. For example the H1 and the P.
3. Save the changed content.
4. For Nano, Ctrl-O Enter will save the file.
5. Stay in the editor. This is important.
6. Each time you save the file, the browser will reload.

### The livereload REPL

1. The server READS your saved file.
2. The server EVALUATES your saved file.
3. The browser PRINTS your saved file.
4. The editor stays open throught the input LOOP.
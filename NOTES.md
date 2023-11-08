# Linomath notes

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
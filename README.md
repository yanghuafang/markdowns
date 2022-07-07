**How to preview Markdown+LaTex on github?**
1. Add file _config.yml with the following two lines:
```
theme: jekyll-theme-cayman
markdown: kramdown
```
2. On top of the Markdown file, add the following lines:
```
<head>
    <script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
    <script type="text/x-mathjax-config">
        MathJax.Hub.Config({
            tex2jax: {
            skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'],
            inlineMath: [['$','$']]
            }
        });
    </script>
</head>
```
3. Preview by VS Code plugin "Markdown Preview Enhanced" by clicking
<kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>V</kbd>
4. Right click the preview page, Select **HTML** -> **HTML (cdn hosted)** to
generate HTML file in current path.
5. git push Markdown file, _config.yml and HTML file to github.
6. Preview HTML through htmlpreview.github.io
``` https://htmlpreview.github.io/?<github HTML file path> ``` e.g.
<https://htmlpreview.github.io/?https://github.com/yanghuafang/markdowns/blob/master/vector-rotation.html>

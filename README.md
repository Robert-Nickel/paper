__Use this as a template for writing your paper. It will automatically build a cool HTML that contains all your citations like [here](https://robert-nickel.github.io/paper).__

1. Install [pandoc](https://pandoc.org/installing.html) (prerequisite!)
2. Fork and clone this repo
3. Write your paper (in `paper.md`)
4. Add citations by adding
   1. the book/article/.. you cite in bibliography.bib
   2. [@citation_handle] in your text
5. Make a git commit. (A pre-commit hook will generate your HTML automatically.)
6. (Optional) If you want to rename `paper.md`, rename it's reference in `.git/hooks/pre-commit` as well
7. (Optional) If you want to generate your HTML without commiting, execute `pandoc --citeproc paper.md --standalone -o index.html`
8. (Optional) If you want your paper to be accessible as a website, activate [Github Pages](https://pages.github.com/) by going to Settings -> GitHub Pages and selecting Master as source branch

Tooling proposal:
- [Visual Studio Code](https://code.visualstudio.com/)
- VSC Extensions
  - [Pandoc Citer](https://marketplace.visualstudio.com/items?itemName=notZaki.pandocciter)
  - [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)
  - [bibtexLanguage](https://marketplace.visualstudio.com/items?itemName=phr0s.bib)
- [Brain](https://en.wikipedia.org/wiki/Brain)

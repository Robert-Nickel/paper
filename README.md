__Use this as a template for writing your paper. It will automatically build a cool HTML that contains all your citations like [here](https://robert-nickel.github.io/paper).__

1. Install [pandoc](https://pandoc.org/installing.html) (prerequisite!)
2. Use this [repo as template](https://docs.github.com/en/free-pro-team@latest/github/creating-cloning-and-archiving-repositories/creating-a-repository-from-a-template#creating-a-repository-from-a-template) (!= fork)
3. Copy `pre-commit` into your `.git/hooks` folder
4. Write your paper (in `paper.md`)
5. Add citations by adding
   1. the book/article/.. you cite in bibliography.bib
   2. [@citation_handle] in your text
6. Make a git commit. (The pre-commit hook will generate your HTML automatically.)
7. If you want to rename `paper.md`, rename it's reference in `.git/hooks/pre-commit` as well
8. If you want to generate your HTML without commiting, execute `pandoc --citeproc paper.md -s --shift-heading-level-by=1 -o index.html`
9. If you want your paper to be accessible as a website, activate [Github Pages](https://pages.github.com/) by going to Settings -> GitHub Pages and selecting Master as source branch
10. If the links in your table of contents in the generated HTML don't work, check if they start with a number. If they do, remove the numbers and use an ordered list instead.
11. If you want to generate a PDF out of that markdown, ensure you have a pdfEngine installed (e.g. MacTex by `brew cask install mactex`), then delete your table of contents from the markdown (it will be generated) and execute `pandoc --citeproc --toc paper.md -o paper.pdf`

Tooling proposals:
- [Visual Studio Code](https://code.visualstudio.com/)
- VSC Extensions
  - [Pandoc Citer](https://marketplace.visualstudio.com/items?itemName=notZaki.pandocciter)
  - [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)
    - Required to auto-generate the table of contents on saving
    - Set the feature "Toc: Ordered List" to true by opening Preferences -> Settings -> Extensions to avoid broken links in table of contents.
  - [bibtexLanguage](https://marketplace.visualstudio.com/items?itemName=phr0s.bib)

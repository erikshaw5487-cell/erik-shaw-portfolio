# Erik Shaw — Portfolio

Static personal site for GitHub Pages. Dark institutional layout. No build step.

Live target: [https://erikshaw5487-cell.github.io/erik-shaw-portfolio/](https://erikshaw5487-cell.github.io/erik-shaw-portfolio/)

- Email: [erikshaw5487@gmail.com](mailto:erikshaw5487@gmail.com)
- GitHub: [erikshaw5487-cell](https://github.com/erikshaw5487-cell)
- LinkedIn: [erik-shaw-37536144a](https://www.linkedin.com/in/erik-shaw-37536144a/)

## Local preview

```bash
python -m http.server 8080
```

Open [http://localhost:8080](http://localhost:8080).

## Publish on GitHub Pages

Must be pushed from the `erikshaw5487-cell` GitHub account.

```bash
gh auth login
git add .
git commit -m "Add personal portfolio site."
git branch -M main
gh repo create erik-shaw-portfolio --public --source=. --remote=origin --push
gh api -X POST repos/erikshaw5487-cell/erik-shaw-portfolio/pages -f build_type=legacy -f source='{"branch":"main","path":"/"}'
```

The site will be at `https://erikshaw5487-cell.github.io/erik-shaw-portfolio/`.

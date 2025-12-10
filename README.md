[https://ben-mess.com/](https://ben-mess.com/)

```bash
conda env create -f quarto_website_env.yml
conda activate quarto_website

# Install non-conda R packages
R
install.packages("bs4cards")
q()

# Install Quarto (if not already installed)
brew install --cask quarto

# Clear Quarto build artifacts (optional before preview)
rm -rf _freeze/ _site/ site/

# Preview site locally
quarto preview
```

Netlify watches for commits, performs the build, and keeps it updated.

Before commit, remove `_freeze/`, `_site/`, and `site/`, then do `quarto preview`, then commit to deploy.

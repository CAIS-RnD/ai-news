Hello! This is a draft for a newsletter.

to commit:

git add issues/issue-02.qmd (trivially for all files)

git commit -m "Publish Issue 02: [Topic Summary]"

git push origin main

to avoid spinning up the server for small changes: ("[skip ci]")
...
git commit -m "Update instructions in README [skip ci]"
git push origin main

for spacing in the md files:

"<div style="height: 40px;"></div>"

or

"<br>"

"quarto preview" i terminalen för att kika utan att behöva pusha





## Publishing an issue or report

Add the source under `issues/` and shared images and PDFs under `assets/`.
Use a numbered newsletter title, authors, an ISO publication date (`YYYY-MM-DD`),
categories, and a short description in the YAML front matter. The archive sorts
entries by date, newest first.

Set `image:` explicitly to choose the archive thumbnail, for example:

```yaml
image: ../assets/3-fno/front_page.png
```

Without `image:`, Quarto uses the first article image. Images inside a PDF iframe
are not available to the listing. Link to other articles using their `.qmd` paths
so Quarto can resolve the output URLs. Declare embedded PDFs under `resources:`
to ensure they are copied to the published site, and include a visible PDF link
for readers who cannot use the embedded viewer.

Run `quarto render` to check the site or `quarto preview` to review it locally.
Pushing to `main` triggers the GitHub Pages publishing workflow.

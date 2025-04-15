## create directory map of whole repo.

> since github pages doesn't support directory listing, we use this directory to manually generate the listing and serve index from /l/

- make sure the listing directories dont have problematic folders like .git and other unwanted files and folders:
`find . \( -name ".git" -o -name ".vscode" -o -name ".gitignore" \) -prune -exec rm -rf {} \;`

- run `php generate_listings.php`
_This will generate directory listing index for each directory that do not contain index.html file_

- push

## create directory map of whole repo.

> since github pages doesn't support directory listing, we use php code to manually generate the listing and serve index from /l/tree/

- make sure the listing directories dont have problematic folders like .git and other unwanted files and folders:
`find . \( -name ".git" -o -name ".vscode" -o -name ".gitignore" \) -prune -exec rm -rf {} \;`

- run `php tree/generate_listings.php`
_This will generate directory listing index for each directory that do not contain index.html file_

- in case things go south and the php script saves tree in incorrect places, undo it with:
`find . -type f -name "index.html" -exec grep -l "<title>Directory:" {} \; -delete`

- push

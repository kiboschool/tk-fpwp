# Future Proof with Python

Uses https://rust-lang.github.io/mdBook/

- Book content is in `/book`
- Notion export is in `/notion-export`

## Getting Started

Install mdbook: https://rust-lang.github.io/mdBook/guide/installation.html

if you use rust:

```
cargo install mdbook
```

Or use your package manager: `brew install mdbook`, or download a release from
Github.

## Run the book locally

```
cd book
mdbook serve --open
```

## Goals

- script the conversion from notion export to mdbook format
- do not modify any of the notion export in place, only put into the book/src

## Notion steps

- Navigate to the root notion page of the export
- click 'export' from the menu
- unzip the folder, move it here, call it ./notion-export 

## Convert

```
./convert.rb
```

This recursively walks the notion export files, cleaning them up as it goes:
- renames the files to use a sanitized slug
- fixes the filenames in the markdown files
- creates the SUMMARY.md file that mdbook uses
- re-srcs the img tags with the new file locations

And it fixes (by matching and replacing on regexes) notion export issues with:
- titles - removes leading numbers / "lesson 0"
- slugs - removes leading numbers to match titles
- asides
- youtube embeds
- loom embeds
- replit embeds
- typeform
- padlet
- google forms
- google docs / slides

- TODO: long tail of content that exports from Notion poorly
  - tables
  - emphasized text
  - blockquotes that don't quote right
  - side-by-side stuff isn't side-by-side anymore
  - toggle blocks are just lists now (instead of details / summary)
  - mp4

## Deploy

Pushes to the `main` branch will automatically deploy to vercel. 

Vercel serves the static content from the `book/output` directory. Run `mdbook
build` to update the build output.

### Manual deployment

You'll need vercel permissions.

Create a preview deploy:

```
vercel
```

Deploy to production:

```
vercel --prod
```

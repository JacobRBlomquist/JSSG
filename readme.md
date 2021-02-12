# Jacob's Static Site Generator

## Written in POSIX compliant shell.

Generates a static site with the following features:

- Header and footer templates
- Sitemap XML
- JSSGIGNORE functionality
- Auto-generated article list

Idea from [Roman Zolotarev](https://www.romanzolotarev.com/ssg.html).

## Usage

```sh
$ chmod +x ./JSSG
$ ./JSSG src dst title base_url
```

- `src` - Source directory where templates and raw md/html files are kept.
- `dst` - Destination directory where **JSSG** will place the rendered site.
- `title` - Title for overall site.
- `base_url` - Base URL for site (used for generating links)

## Templates

To use header and footer templates, create files titled `\_footer.html` and `\_footer.html` within the `src` directory. Every generated page will
have these appended to their HTML.

## Auto-generated article list

In your `index.html` file place the following tag anywhere to generate a list of articles with links.

```
</article>
```

Files that contain `index` and `contact` are excluded. The link name is determined by the contents of an `h1` tag which MUST be the first line of the article html files.

## Dependencies

### CPIO

#### Arch

```sh
$ sudo pacman -S cpio
```

#### Debian

```sh
$ sudo apt-get install cpio
```

#### Redhat

```sh
$ sudo yum install cpio
```

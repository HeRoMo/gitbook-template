# Gitbook template

A Gitbook project template.
This template has the following features,

- PlamntUML support, using [bitjourney/plantuml\-service](https://hub.docker.com/r/bitjourney/plantuml-service).
- Ready for output PDF, EPUB and MOBI files.
- Configured VSCode Tasks and Recommended extensions.

## Dependencies

### Required
- [Docker](https://www.docker.com/products/docker-desktop)
### Recommended
- [Visual Studio Code](https://code.visualstudio.com/)
- [LiveReload](https://chrome.google.com/webstore/detail/livereload/jnihajbhpnppcggbcgedagnkighmdlei): Chrome Extention

## Usage

This Docker image for gitbook is manage markdown files in *gitbook* directory.

### Initialize

Run the following command, to init your gitbook

```bash
$ curl https://codeload.github.com/HeRoMo/gitbook-template/zip/master -O
$ unzip master
$ mv gitbook-template-master your-gitbook-name
$ cd your-gitbook-name
$ docker-compose run --rm gitbook init
```

After init, *gitbook* directory will be created.
If you want, modify gitbook/book.json for your gitbook.

### Run local server

Run the following command, to start gitbook server.

```bash
$ docker-compose up
```

Open http://localhost:4000, after docker containers are started.

If you use [Chrome](https://www.google.co.jp/chrome/) browser with [LiveReload](https://chrome.google.com/webstore/detail/livereload/jnihajbhpnppcggbcgedagnkighmdlei) extention, Reload automatically after modify *.md files.

### Output PDF, EPUB and Mobi files

Run the following command, output PDF file as *book.pdf*

```bash
$ docker-compose run --rm gitbook pdf
```

Run the following command, output EPUB file as *book.epub*

```bash
$ docker-compose run --rm gitbook epub
```

Run the following command, output MOBI file as *book.mobi*

```bash
$ docker-compose run --rm gitbook mobi
```

## Related Project
- [hero/gitbook \- Docker Hub](https://hub.docker.com/r/hero/gitbook)

## License

MIT. see [LICENSE](./LICENSE)

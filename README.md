![github-ps-delivery-48](https://user-images.githubusercontent.com/2089743/185767087-4ac37f9d-83dd-4b42-ba04-402279ca3bda.jpg)

# gh-montage

A `gh` extension to generate GitHub user avatar montage from an organization or organization team.

I must give thanks to [@martinwoodward](https://github.com/martinwoodward) because [his gist](https://gist.github.com/martinwoodward/288812fa142e0b1153f60b9555b3d978) was the foundation for this extension!  Thank you so much, Martin, for finding creative and clever ways to showcase GitHub users! :bow:

## Quickstart

1. Download and install [ImageMagick][imagemagick] 7.1.0 or newer
   - [Linux][imagemagick-download-linux]
   - [Mac OS][imagemagick-download-macos]
   - [Windows][imagemagick-download-windows]
1. `gh extension install andyfeller/gh-montage`
1. `gh montage <organization>`
1. Profit! :moneybag: :money_with_wings: :money_mouth_face: :money_with_wings: :moneybag:

## Usage

> **Note**
> Processing username files assumes 1 username per line and will fail if any username is invalid.
> This is because `gh-montage` is not retrieving usernames from GitHub API before processing them.

```shell
$ gh montage --help

Generate montage from GitHub user avatars.

USAGE
  gh montage [options] <organization>
  gh montage [options] <organization>/<team>
  gh montage [options] <path/to/username file>

FLAGS
  -a, --avatar-pixels <integer>       Size of GitHub avatar icons in pixels; default '48'
  -d, --debug                         Enable debugging
  -f, --force                         Whether to overwrite output file if it exists
  -h, --help                          Displays help usage
  -m, --montage-width <integer>       Width of GitHub montage in number of avatar icons; default '58'
  -o, --output-file <output-file>     Name of GitHub montage file to generate, without '.jpg' extension
  -p, --preserve                      Preserve temporary directory containing data
```

## Setup

Like any other `gh` CLI extension, `gh-montage` is trivial to install or upgrade and works on most operating systems:

- **Installation**

  ```shell
  gh extension install andyfeller/gh-montage
  ```
  
  _For more information: [`gh extension install`](https://cli.github.com/manual/gh_extension_install)_

- **Upgrade**

  ```shell
  gh extension upgrade gh-montage
  ```

  _For more information: [`gh extension upgrade`](https://cli.github.com/manual/gh_extension_upgrade)_

[ImageMagick][imagemagick] 7.1.0-45 was used at the time of development and is likely the most involved depending on your operating system:

- [Linux][imagemagick-download-linux]
- [Mac OS][imagemagick-download-macos]
- [Windows][imagemagick-download-windows]

[imagemagick]: https://imagemagick.org
[imagemagick-download-linux]: https://imagemagick.org/script/download.php#linux
[imagemagick-download-macos]: https://imagemagick.org/script/download.php#macosx
[imagemagick-download-windows]: https://imagemagick.org/script/download.php#windows

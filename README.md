# Git Skeleton

## Introduction

A skeleton project. Feel free to fork and adapt. Pull requests welcome.

## Usage

The following command:

- Asks for an installation directory
- Asks for a skeleton origin URL
- Clones the origin
- Overwrites installation directory with src/ directory
- Initialises an empty Git repository in the installation directory

``` bash
(ORIGIN="https://github.com/markchalloner/git-skeleton" && \
echo -n "Installation directory (use . for current): " && read TARGET && \
git clone "${ORIGIN}" "${TARGET}" && \
find "${TARGET}" -mindepth 1 -maxdepth 1 ! \( -name 'src' -o -name '.' -o -name '..' \) -exec rm -rf {} \; && \
shopt -s dotglob && mv "${TARGET}/src/"* "${TARGET}" && rm -rf "${TARGET}/src" && \
cd "${TARGET}" && git init && \
echo "Done. Have a nice day")

```

Once checked out update the follwoing files with the project name (search `{project}`):

- [CHANGELOG](src/CHANGELOG.md)
- [CONTRIBUTING](src/CONTRIBUTING.md)

## Change log

Please see [CHANGELOG](CHANGELOG.md) for more information what has changed recently.

## Contributing

Please see [CONTRIBUTING](CONTRIBUTING.md) for details.

## Credits

- [Mark Challoner][link-author]
- [All Contributors][link-contributors]
- [PHP League Skeleton][link-phpleague]

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.

[link-author]: https://github.com/markchalloner
[link-contributors]: ../../contributors
[link-phpleague]:  https://github.com/thephpleague/skeleton


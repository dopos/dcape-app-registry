# dcape-app-registry
Private docker registry for dcape users

[![GitHub Release][1]][2] [![GitHub code size in bytes][3]]() [![GitHub license][4]][5]

[1]: https://img.shields.io/github/release/dopos/dcape-app-registry.svg
[2]: https://github.com/dopos/dcape-app-registry/releases
[3]: https://img.shields.io/github/languages/code-size/dopos/dcape-app-registry.svg
[4]: https://img.shields.io/github/license/dopos/dcape-app-registry.svg
[5]: LICENSE

[Docker registry](https://github.com/distribution/distribution) application package for [dcape](https://github.com/dopos/dcape).
Access to registry is limited by [gitea](https://gitea.io) users the same way as to other private [dcape](https://github.com/dopos/dcape) resources.

## Docker image used

* [registry](https://hub.docker.com/_/registry)

## Requirements

* linux 64bit (git, make, wget, gawk, openssl)
* [docker](http://docker.io)
* [dcape](https://github.com/dopos/dcape)
* [gitea](https://gitea.io)

## Usage

* Gitea: Fork or mirror this repo in your Git service
* Drone: Activate repo
* Gitea: "Test delivery", config sample will be saved to enfist
* Enfist: Edit config and remove .sample from name
* Gitea: "Test delivery" again (or Drone: "Restart") - app will be installed and started on webhook host

## TODO

* [ ] send image prefix to narra and check its presense in user's organizations list

## See also

* [Deploy apps with dcape](https://dopos.github.io/dcape/usage/apps/)

Other ways to get private docker registry

* for docker registry: https://github.com/cesanta/docker_auth [out of time](https://github.com/cesanta/docker_auth/issues/288#issuecomment-702931777)
* https://github.com/goharbor/harbor
* http://port.us.org/ (wait for gitea support [here](http://port.us.org/features/oauth.html))

## License

The MIT License (MIT), see [LICENSE](LICENSE).

Copyright (c) 2022 Aleksey Kovrizhkin <lekovr+dopos@gmail.com>

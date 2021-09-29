# VS Code Remote Containers

## List of containers

* [electron](electron)

## Container building

The images in this repository are being built automatically using  [build-push-action](https://github.com/docker/build-push-action) and [github-script](https://github.com/actions/github-script) Github actions.

### Add a new image

1. Create a new subfolder (*image*)
2. Place *Dockerfile* into *image* folder 
3. Create a github personal token at github.com and put it in `GH_TOKEN` environment variable
4. `echo $GH_TOKEN | docker login ghcr.io -u github_user --password-stdin`
5. `docker build -t ghcr.io/soloai/vscode-devcontainers-image:scratch .`
6. `docker push ghcr.io/soloai/vscode-dev-containers-image:scratch`
7. Go to github.com and allow Github actions to write packages and change visibility for the image
## License

Copyright (c) Solo AI Organisation. All rights reserved.

Licensed under the MIT License. See [LICENSE](LICENSE).
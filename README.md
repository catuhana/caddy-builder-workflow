# Caddy

Custom builds of Caddy server built by GitHub Actions with xcaddy.

## Why?

To build custom Docker images / binaries of Caddy with plugins if preferred.

I am aware that we can just build it on a host machine with [the same way as this repository does](.github/workflows/build-and-release.yaml#L100-L108), but the reason I wanted to leverage GitHub Actions is I didn't have a powerful enough machine to build Caddy for Docker every time.

## How to Build Caddy Myself Using This?

If you want a custom build of Caddy with a plugin you want, you can just create an issue about it and I will build it. But if you'd like to have your own builds, just fork the repo, go to GitHub Actions page, enable actions and just dispatch the workflow.

> [!WARNING]
>
> You might want to remove the line `tuhana/${{ env.IMAGE_NAME }}` on the workflow file to prevent Docker image push errors. This will only push the image to GitHub Container Registry, skipping Docker Hub.

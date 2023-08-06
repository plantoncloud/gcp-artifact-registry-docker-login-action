# Docker Build and Push GitHub Action

This GitHub Action allows you to build a Docker image and push it to a specified Docker repository using credentials from Artifact-Store on Planton Cloud.

## Usage

You can include the action in your workflow to take advantage of its capabilities.

```yaml
uses: plantoncloud/build-and-push-docker-image-action@main
with:
  planton_cloud_artifact_store_id: '<id-of-the-artifact-store-on-planton-cloud>'
  docker_repo_hostname: '<hostname-of-the-docker-repository'
  container_image_repo: '<repo-of-the-docker-image-to-be-built-and-pushed>'
  container_image_tag: '<tag-of-the-docker-image-to-be-built-and-pushed>'
```

### Inputs

- `planton_cloud_artifact_store_id`: This is the ID of the Artifact Store on Planton Cloud. It is a required input.
- `docker_repo_hostname`: This is the hostname of the Docker repository. It is a required input.
- `container_image_repo`: This is the repo of the Docker image to be built and pushed. It is a required input.
- `container_image_tag`: This is the tag of the Docker image to be built and pushed. It is a required input.

## How it works

This action performs the following steps:
- Fetch the Artifact Store key from Planton Cloud service
- Login to the Docker registry using the fetched key
- Build the Docker image using the provided image repo and tag
- Push the Docker image to the specified Docker repository

# Login to GCP Artifact Registry Docker Repo Action

This GitHub action fetches an Artifact Store writer key from Planton Cloud and uses it to log in to the specified Docker repository in the Google Cloud Platform's Artifact Registry.

## Inputs

### `planton_cloud_artifact_store_id`

**Required** ID of the Artifact Store on Planton Cloud.

### `docker_repo_hostname`

**Required** Hostname of the Docker repository in the Google Cloud Platform's Artifact Registry.

## Usage

```yaml
steps:
  - name: Login to GCP Artifact Registry Docker Repo
    uses: plantoncloud/gcp-artifact-registry-docker-login-action@main
    with:
      planton_cloud_artifact_store_id: your-artifact-store-id
      docker_repo_hostname: your-docker-repo-hostname
```

After executing this action, the runner will be authenticated and able to interact with the specified Docker repository in the Google Cloud Platform's Artifact Registry using the fetched writer key from Planton Cloud.

## Contributing

If you have suggestions for how this GitHub Action could be improved, or want to report a bug, open an issue! We'd love all and any contributions.

## License

This project is licensed under the [MIT License](LICENSE).

# setup-seqerakit

A Github Action to set up everything needed to run [`seqerakit`](https://github.com/seqeralabs/seqera-kit), including setup of [`tower-cli`](https://github.com/seqeralabs/tower-cli) if not found already in the Github Action runner environment.
## Usage

```yml
  - name: Compare coverage
    uses: alvaromartmart/setup-seqerakit@v1
    with:
      api-endpoint: "https://tower.nf/api"
      token: ${{ secrets.SEQERA_PLATFORM_PERSONAL_ACCESS_TOKEN }}
  - name: Use seqerakit
    run: |
      seqerakit my_data.yml
```

### Action inputs

| Name | Description | Default |
| --- | --- | --- |
| `token` | Personal access token defined in Seqera Platform. Store it as a Github secret to avoid disclosing it. | - |
| `api-endpoint` | Seqera platform API endpoint | https://tower.nf/api


#### Outputs

None

## License

[MIT](LICENSE)
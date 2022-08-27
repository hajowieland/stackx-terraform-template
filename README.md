# stackx-template-terraform

Template repository for Terraform used by all our stackx GitHub repositories.

This repo will be synced with the
[AndreasAugustin/actions-template-sync](https://github.com/AndreasAugustin/actions-template-sync) GitHub Action.


## Requirements

### API Keys
During setup of the new GitHub repository, set these [Secrets for GitHub Actions](https://docs.github.com/en/actions/security-guides/encrypted-secrets#creating-encrypted-secrets-for-a-repository):

* `INFRACOST_API_KEY`
* `LOCALSTACK_API_KEY`

> For modules without LocalStack support, please set `LOCALSTACK_API_KEY` 
> to `false`


### Diagrams

Add a `diagram.py` in `docs/images` to automatically generate a 
[diagram as code](https://diagrams.mingrammer.com).

The required syntax (replace `repository-name` accordingly:

```python
with Diagram("repository-name", outformat="png", filename="screenshot1", show=False):
```


### README

Create a `README.yaml` in the `docs/` subdirectory, which will be used in the 
[stackx-action-readme-templates](https://github.com/ventx/stackx-action-readme-templates) 
GitHub Action to generate the final README.md file.

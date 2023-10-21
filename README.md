# stackx-template-terraform

Template repository for Terraform used by all our stackx GitHub repositories.

This repo will be synced with the
[AndreasAugustin/actions-template-sync](https://github.com/AndreasAugustin/actions-template-sync) GitHub Action.


## Requirements

### Secrets
During setup of the new GitHub repository, set these [Secrets for GitHub Actions](https://docs.github.com/en/actions/security-guides/encrypted-secrets#creating-encrypted-secrets-for-a-repository):

* Set `APP_ID` and `PRIVATE_KEY` for the ventx-Bot GitHub App
* Set cloud-specific Secrets

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


### Pull Request Labels

Add the following labels to your repository if they are not already there:

* `chore`
* `ci`
* `docs`
* `template-sync`
* `terraform`

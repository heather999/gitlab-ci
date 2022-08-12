# gitlab-ci

## GitHub Setup

Mirroring code from GitHub to GitLab

* Personal Access Token https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token
In this example MIRROR_SOURCE_PAT

Check both Masked and Protected in GitLab mirror repo

To write to GitLab another PAT needs to be set up

https://software.nersc.gov/NERSC/nersc-ci-docs/-/wikis/Home#interacting-with-a-repository-through-api
MIRROR_TARGET_PAT

Check both Masked and Protected

No need to create the repo in GitLab - the first time the mirror is run will do that for you.


On the GitLab copy of the repo - set up a Pipeline Trigger Token (under Settings->CI/CD->Pipeline Tokens) that will be stored in the GitLab mirror repo CI/CD variables  See: https://software.nersc.gov/help/ci/triggers/index.md
<repo>_TRIGGER_TOKEN also Masked and Protected in the GitLab mirror CI/CD Variables

# Set up .gitlab-ci.yml in your GitHub repo
  

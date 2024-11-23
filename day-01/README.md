# Create a GitHub Repository & Push the First Commit

## Create Repository
- Login into GitHub at https://github.com/Astrotope
- Click 'Repositories' in the top-left menu.
- Click the green 'New' button.
- Choose 'Owner*' if not already selected.
- Give the repository a name in 'Repository name*'
- Add a description in 'Description (optional)'.
- Click the 'Create Repository' button.

## Create a Repository Scoped PAT

- Click profile image icon top-right menu.
- Click 'Settings'
- Click '<> Developer settings' in righthand menu.
- Click 'Personal access tokens' drop-down.
- And select 'Fine-grained tokens (Preview)'.
- Click 'Generate new token' button.
- Authenticate. If 2FA is setup, enter 'Authentication Code' from authenticator app (Authy in my case). And click 'Verify' if needed.
- Give the token a name (suggest '[repo-name-abbreviated]-[conwr-prwr]-[expire-date]' i.e. name-permissions-expire). Limited no. of character available, so keep it short.
- Give the token a description - 'Developer Token for [repo-name] expires Dec 23, 2024'.
- Under 'Repository access' select 'Only select repositories', and choose repository to create PAT for. i.e. Astrotope/[repo-name].
- Under 'Permissions' expand 'Repository permissions'.
- For developers you will need to set the following permissions to R/W
  - Contents - Read and Write
  - Pull requests - Read and Write
  - And only if needed - Workflows - Read and Write (Care should be taken, with who this permission is given to.)
- Click the green 'Generate token' button.
- Back in the 'Fine-grained personal access tokens' screen, click the the copy icon under 'Make sure to copy your personal access token now as you will not be able to see this again'.
- Paste the token somewhere secure so that you can access it again (like a password or secrets manager). The token should look something like 'github_pat_[rest-of-token]'.

## Make First Commit to the Repository

```
mkdir [repository-name] && cd [repository-name]
echo "# [Heading Text]" >> README.md
git init
git add .
git commit -m "add READEM.md"
git branch -M main
git remote add origin https://<PAT>@github.com/Astrotope/<repo_name>.git
git push -u origin main
```


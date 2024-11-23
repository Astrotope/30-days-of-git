# Create a GitHub Repository & Push the First Commit

## Create Repository
(1) Login into GitHub at https://github.com/Astrotope
(2) Click 'Repositories' in the top-left menu.
(3) Click the green 'New' button.
(4) Choose 'Owner*' if not already selected.
(5) Give the repository a name in 'Repository name*'
(6) Add a description in 'Description (optional)'.
(7) Click the 'Create Repository' button.

## Create a Repository Scoped PAT

(1) Click profile image icon top-right menu.
(2) Click 'Settings'
(3) Click '<> Developer settings' in righthand menu.
(4) Click 'Personal access tokens' drop-down.
(5) And select 'Fine-grained tokens (Preview)'.
(6) Click 'Generate new token' button.
(7) Authenticate. If 2FA is setup, enter 'Authentication Code' from authenticator app (Authy in my case). And click 'Verify' if needed.
(8) Give the token a name (suggest '[repo-name-abbreviated]-[conwr-prwr]-[expire-date]' i.e. name-permissions-expire). Limited no. of character available, so keep it short.
(9) Give teh token a description - 'Developer Token for [repo-name] expires Dec 23, 2024'.
(10) Under 'Repository access' select 'Only select repositories', and choose repository to create PAT for. i.e. Astrotope/[repo-name].
(11) Under 'Permissions' expand 'Repository permissions'.
(12) For developers you will need to set the following permissions to R/W
  - Contents - Read and Write
  - Pull requests - Read and Write
  - And only if needed - Workflows - Read and Write (Care should be taken, with who this permission is given to.)
(13) Click the green 'Generate token' button.
(14) Back in the 'Fine-grained personal access tokens' screen, click the the copy icon under 'Make sure to copy your personal access token now as you will not be able to see this again'.
(15) Paste the token somewhere secure so that you can access it again (like a password or secrets manager). The token should look something like 'github_pat_[rest-of-token]'.

## Make First Commit to the Repository

(1) mkdir [repository-name] && cd [repository-name]
(2) echo "# [Heading Text]" >> README.md
(3) git init
(4) git add .
(5) git commit -m "add READEM.md"
(6) git branch -M main
(7) git remote add origin https://<PAT>@github.com/Astrotope/<repo_name>.git
(8) git push -u origin main


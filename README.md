# praxis
Guide:
- Personal Access Token
  - Ensure that you are logged into Github.
  - Visit https://github.com/settings/tokens
    - Create new token with only "public_repo" scope selected.
    - Delete when no longer needed.
  - Set your token as an environment variable.
  - Set your username as an environment variable.
- practice repository
  - Set this repo's "owner" as an environment variable. (euggo)
  - Set this repo's "name" as an environment variable. (praxis)
- "github" library
  - Should not have any credentials hardcoded.
  - Should implement Create, Read, Update, Lock, Unlock, and Search.
  - Should make using it's API as convenient as possible.
- "main" application
  - Should pull credentials (user, token, owner, repo) from environment variables.
  - Should generally make use of your github library.
  - *User/Token usage: https://golang.org/pkg/net/http/#Request.SetBasicAuth
  - *User/Token advanced: https://stackoverflow.com/questions/16673766/basic-http-auth-in-go
  - *Pin Github API ver `req.Header.Set("Accept", "application/vnd.github.v3.text-match+json"))`
  - *Documentation is your friend: https://developer.github.com/v3/                                                             
    - We're particularly interested in "issues" (https://developer.github.com/v3/issues/) 

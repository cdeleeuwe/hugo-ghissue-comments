# Github issues as Hugo comments

Example of fetching GitHub issue comments on Hugo build. Issues can be defined in 2 ways.
1. By defining the number in the page's Frontmatter
2. By matching the issue and page's title

### Config
* **comments_repo**: The repository name to fetch from
* **enable_auth**: To add GitHub auth, since unauthenticated api calls are limited to 60/hour and authenticated 5000/hour. See https://developer.github.com/v3/#rate-limiting. To enable auth, add the following 2 environment variables:
  * GITHUB_CLIENT_ID
  * GITHUB_CLIENT_SECRET

### To run

with auth:
```
GITHUB_CLIENT_ID=YOUR_CLIENT_ID GITHUB_CLIENT_SECRET=YOUR_CLIENT_SECRET hugo server --ignoreCache
```

without auth:
```
hugo server --ignoreCache
```

> NOTE: --ignoreCache is optional

### Demo

[hugo-gh-comments.netlify.com](https://hugo-gh-comments.netlify.com)

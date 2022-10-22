# Leadership Journey Website

My thoughts and experiences on leadership. Hosted at https://www.leadershipjourney.io.

This website uses Hugo static website generator.

### A couple of things I learned as I was setting this site up:

- Place `CNAME` file under `static` folder with the domain name inside looking like `www.leadershipjourney.io`. Otherwise, the Github Action overwrites and deletes the `CNAME` file and you need to set it up manually again on Setttings > Page page. Adding a custom domain automatically adds `CNAME` file in the repository.
- Running `hugo` command builds the website, but if you want to see the changes quickly, run `hugo server` command, which boths watches the changes and automatically rebuilds the website.
- You need to add the following `CNAME` entry to your domain's DNS settings as the second one is required for the custom domain to work:
    - `CNAME @ tarikguney.github.io`
    - `CNAME www tarikguney.github.io`
- Addding a new page is done by running `hugo new --kind post posts/name-of-the-post.md` and `.md` extension is required as it is one of the archetypes.
- If you are using Cloudflare, by adding the following page rules, you can have HTTPS and www redirection work:
    - http://leadershipjourney.io/* -> Always Use HTTPS
    - https://leadershipjourney.io -> Forwarding URL -> https://www.leadershipjourney.io
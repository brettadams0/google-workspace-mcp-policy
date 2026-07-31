# google-workspace-mcp-policy

The homepage and privacy policy that Google's OAuth consent screen requires, for the OAuth client
behind [`google-workspace-mcp`](https://github.com/brettadams0/google-workspace-mcp).

Live at <https://brettadams0.github.io/google-workspace-mcp-policy/>.

## Why this is a separate repo

Google will not verify an OAuth client without a publicly reachable homepage and privacy policy on a
domain you can demonstrate ownership of, and both URLs have to keep resolving for as long as the
client exists. Keeping them here — plain static HTML on GitHub Pages, in their own repo — means the
consent screen's requirements are not coupled to anything in the server's own release cycle.

| File | |
|---|---|
| `index.html` | Homepage: what the app is, and why each OAuth scope is requested |
| `privacy.html` | Privacy policy: what data is touched, what is stored, and where |
| `googlecc9821fbd61b8a24.html` | Google Search Console domain-verification token |

No build step and no dependencies. GitHub Pages serves the files as they are; edit and push.

## If you change the scopes

`index.html` lists each scope with a justification, and reviewers compare that list against what the
client actually requests. Change the scopes in `google-workspace-mcp` and this page has to change in
the same pass, or verification falls out of sync with reality.

## License

MIT — see [LICENSE](LICENSE).

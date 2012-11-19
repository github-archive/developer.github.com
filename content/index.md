---
title: GitHub API
---

# The GitHub API

This describes the resources that make up the official GitHub API v3. If
you have any problems or requests please contact
[support](mailto:support@github.com?subject=APIv3).

For the new API v3, start browsing the resources on the right >>

View the [API Changelog](#changes) for information on existing and
planned changes to the API.

To get started, [create an API key](https://github.com/settings/applications/new) or [manage your existing API keys](https://github.com/settings/applications).

## Current Version

    Accept: application/vnd.github.beta+json

The GitHub API version is currently in beta.  [The `beta` media type](/v3/media/)
property will be valid until sometime in 2013.  A notice will be given closer
to the actual date.

We consider the "beta" API unchangeable.  [File a support issue](https://github.com/contact)
if you have problems.

#### Expected Changes <a name="changes"></a>

These changes are _not_ implemented, just planned for the next major API version.

* Standardize on existing `*_url` attributes for hypermedia.  Remove all `_links`
objects.
* The `/repos/:owner/:repo/hooks/:id/test` action becomes
  `/repos/:owner/:repo/hooks/:id/tests`.
* The `/gists/:id/fork` action becomes `/gists/:id/forks`.
* Gist forks/history objects become separate API calls.
* Gist files object is not returned on Gist listings.
* Commit schema will change to be [more consistent](https://gist.github.com/3a2e5779588e21b0c0f3).
* `master_branch` becomes `default_branch`.
* `integrate_branch` on the [repo API](/v3/repos/#get) will no longer be
  returned.
* Use the `private` attribute when creating a private repository,
  instead of setting `public` to false.
* User Emails come back as a hash instead of a string.

        {"email": "email@whatev.com", "state": "verified"}

### Breaking Beta Changes

##### August 30, 2012
* Added `repo:status` scope
* Added Status API

##### August 7, 2012
* Clarified watching/stargazing

##### June 12, 2012:
* Removed API v1 support
* Removed API v2 support

##### June 15th, 2011:

* `gravatar_url` is being deprecated in favor of `avatar_url` for all
  responses that include users or orgs. A default size is no longer
  included in the url.
* Creating new gists (both anonymously and with an authenticated user)
  should use `POST /gists` from now on. `POST /users/:user/gists` is no
  longer supported.

##### June 1st, 2011:

* Removed support for PUT verb on update requests. Use POST or PATCH
  instead.
* Removed `.json` extension from all URLs.
* No longer using the X-Next or X-Last headers. Pagination info is
  returned in the Link header instead.
* JSON-P response has completely changed to a more consistent format.
* Starring gists now uses PUT verb (instead of POST) and returns 204.

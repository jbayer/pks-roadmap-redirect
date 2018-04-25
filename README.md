# Redirect app for the PKS Roadmap

This little Cloud Foundry application does a simple redirect from a vanity URL to a URL configured in the manifest.yml. Note that if the URL is a google doc, that you should append a '?' to the end or the URL may not load properly.

It uses the [staticfile buildpack](https://github.com/cloudfoundry/staticfile-buildpack) to deploy a bespoke `nginx.conf`. That's it.

## Deploy

```
# Update manifest.yml to have the right URL to redirect to.
# Login as a user with access to PWS jwatters-org / staging space.
cf push
```

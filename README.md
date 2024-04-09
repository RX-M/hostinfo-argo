# hostinfo-argo

This repo houses a version of HostInfo meant for deployment via ArgoCD


## Contents

- `charts/hostinfo` - A helm chart directory for HostInfo
- `charts/yamls` - A directory for miscellaneous manifests


## Use

This repo is meant to test a case where ArgoCD is needed to work within the following constraints:

- Track a single repository (no multiple repos)
- Track a single branch (all changes in the `main` branch should be deployed)
- Track environment-specific files (some files are unique to some other environments)

ArgoCD `application` resources can use the files in this Repo to test that case.
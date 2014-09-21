# frigg-ci

# Setup
```
make
```

### Settings that need to be setup
Add these to `frigg.settings.local`.

* `PROJECT_TMP_DIRECTORY` - The location you want frigg to clone and test projects.
* `SERVER_ADDRESS` - To get the correct domain in comments on Github etc.
* `GITHUB_ACCESS_TOKEN` - Token needed to make the project able to post comments on Github.

# Add projects
Add `http://<your frigg domain>/github-webhook` to the projects webhooks on Github.

## Config file
Frigg supports config file to give details about what kind of tasks to perform. The file
should be named `.frigg.yml` and placed in the root of the project.  The fields allowed
in the config is described below:

### `task`
Should be defined as a list of commands. Those commands will be run in the order they are
defined during the run.

### `webhooks`
Should be defined as a list of urls where frigg can post status about the build.

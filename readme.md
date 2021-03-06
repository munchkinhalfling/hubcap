# hubcap
## A package manager for GitHub repositories
Note: Use [app](https://github.com/aleksrutins/app).
### Installation
```sh
$ npm install -g aleksrutins/hubcap
```
### Usage
To install a repository, run `sudo hubcap install <org>/<repo>`. For example, to install Bettermake, use `sudo hubcap install aleksrutins/bettermake`. \
Hubcap installs each program in its own prefix and then symlinks the binaries. Therefore, uninstallation is as easy as `rm -rf`'ing `/usr/local/hubcap/install/<user>/<repo>`. \

### Adding hubcap to your repository
Create a file called `.hubcap/config.yml` in your repository on the `master` branch. See [the one in Bettermake](https://github.com/aleksrutins/bettermake/blob/master/.hubcap/config.yml) for an example and syntax. \
Then, people can install your repo as detailed above. There is no central package submission database or anything, so that is all that is needed.

### Contributing to a repository that uses hubcap
You can install the dependencies of a local project by runing `hubcap depend` in the root directory of the project.

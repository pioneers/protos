# protos

Protobuf message definitions for PiE software. Should be updated by Dawn, Shepherd, and Runtime and imported as a submodule into all three project repositories so that the protobuf definitions don't become out of sync with each other.

See are some tutorials on git submodules:

* [Atlassian](https://www.atlassian.com/git/tutorials/git-submodule)
* [Git-Scm](https://git-scm.com/book/en/v2/Git-Tools-Submodules)

## Usage

When first using submodule, run the following commands on the branch with the submodule set up:

* `git submodule init`
* `git submodule update`

When cloning the entire repo for the first time, you can do the same thing. 

<br>

When this `protos` repo (which is a submodule in other repos) is updated, then all people in projects that include this submodule must run `git submodule update --remote` in order to obtain the latest changes.


## Setting up

Adding this submodule to a repo should only be done by one person. The rest should have to only follow the steps in the "Usage" section.

To add this submodule to a project, first checkout a new branch from `master` on that project. Then do:

* `git submodule add -f https://github.com/pioneers/protos.git <path/to/protos/folder>`

This command creates a file in the root directory of the repo called `.gitmodules` that needs to then be pushed to the repo (should not be ignored). Make sure that any old `protos/` folder or protobuf definitions are removed before doing this.

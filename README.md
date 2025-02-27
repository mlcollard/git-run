# git-run

`git-run` and `git-all` are two scripts that allow you to run the same command across all the git repositories in a directory:

| Script    | Example        | Description |
|:---------:|:---------------|:------------|
| `git-all` | `git all pull` | Run the `git` command for all of the repositories |
| `git-run` | `git run ls`   | Run any command for all of the repositories |

More examples:

* `git all -p pull` - Run the `git pull` command in parallel
* `git all list tag` - Run the `git tag` command on the repositories listed in the file _list_
* `git all -s tag` - Run the `git pull` command with no other output
* `git all -q tag` - Run the `git pull` command showing only the subdirectory name
* `git run -p 'mkdir build; cd build; cmake ..; make; make run'` - Run those bash commands in parallel for each repository

The environment variable GITRUN_JOBS can control the amount of parallelism.

Use `git run --help` to see all the options.

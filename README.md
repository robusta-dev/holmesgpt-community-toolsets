# holmesgpt-community-toolsets
Collection of community contributed [HolmesGPT](https://github.com/robusta-dev/holmesgpt) toolsets


New toolsets are loaded by running HolmesGPT with `-t /path/to/custom/toolset`. Use -t multiple times to add multiple toolsets .

# Community Toolsets in this Repo
## GitHub

When to use this toolset

Example usage:

```
$ holmes ask ...

output of command here
```

[View the toolset's source.](./github)

# Adding Your Own ToolSet
1. Create a new directory with the name of your toolset
2. Put your toolset.yaml file inside of it. Make sure that the toolset has a unique name which wont override existing toolsets!
3. Edit this README.md to add your toolset. Please follow the format of existing toolsets. Make sure that:
* You include a real world `holmes ask` command showing how the toolset can be used (share real world output, but you can sanitize it if necessary)
* You tested the command before opening this PR and verified that the command works


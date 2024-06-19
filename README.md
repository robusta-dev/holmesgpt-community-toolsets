# Community Toolsets for the HolmesGPT OpenSource Agent
Collection of community contributed [HolmesGPT](https://github.com/robusta-dev/holmesgpt) toolsets

New toolsets are loaded by running HolmesGPT with `-t /path/to/custom/toolset`. Use -t multiple times to add multiple toolsets .

# Toolsets in this Repo
## GitHub

When to use this toolset: to investigate failed GitHub actions

Example usage:

```console
$ holmes ask "Can you check the docker build job fail in robusta-dev/experimental-ai-investigation repo" -t examples/github/toolset.yaml
User: Can you check the docker build job fail in robusta-dev/experimental-ai-investigation repo
Running `gh workflow list --all --repo robusta-dev/experimental-ai-investigation`                                                                        tools.py:89
Running `gh run list --workflow 100271757 --repo robusta-dev/experimental-ai-investigation`                                                              tools.py:89
Running `gh api /repos/robusta-dev/experimental-ai-investigation/actions/runs/9290945280/jobs`                                                           tools.py:89
Running `gh run view --job 25568377591 --repo robusta-dev/experimental-ai-investigation --log-failed`                                                    tools.py:89
AI: The Docker build job failed due to a missing config.yaml file. The error occurred during the COPY config.yaml /app/ step in the Dockerfile.

Error:
                    
 ERROR: failed to solve: failed to compute cache key: failed to calculate checksum of ref q5l980c2guz3c2j2oaxes75wd::t7psmav6y8vngu63119mpla4d: "/config.yaml": not 
                                                                                                                                    
Ensure config.yaml exists in the build context.         
```

[Toolset source](./github)

# Adding Your Own Toolset
1. Create a new directory with the name of your toolset
2. Put your toolset.yaml file inside of it. Make sure that the toolset has a unique name which wont override existing toolsets!
3. Edit this README.md to add your toolset. Please follow the format of existing toolsets.
* You must include a real world `holmes ask` command showing how the toolset can be used (share real world output, but sanitize it if necessary)
* You must test the command before opening this PR and verify that the command works


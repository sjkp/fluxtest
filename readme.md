# Install Flux
brew install fluxcd/tap/flux

# Create Git Repo

# Create GitHub fine-grained PAT

Bootstrap can be run with a GitHub fine-grained personal access token, for repositories that are created ahead of time by an organization admin.

The fine-grained PAT must be generated with the following permissions:

    Administration -> Access: Read-only
    Contents -> Access: Read and write
    Metadata -> Access: Read-only

Note that Administration should be set to Access: Read and write when using bootstrap github --token-auth=false.

# Export credentials
export GITHUB_TOKEN=<your-token>
export GITHUB_USER=<your-username>

# Install Rancher Desktop
Use moby 

# Check K3S is ready
flux check --pre


# Initialize Flux repo
```
flux bootstrap github --token-auth \          
  --owner=$GITHUB_USER \
  --repository=fluxtest \
  --branch=main \
  --path=./clusters/maccluster \
  --personal
```
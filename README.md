# cacheGitHubActions

Develop a proof of concept for GitHub Actions that cache the installation of the SF CLI. Doing so will ensure the CI/CD actions run faster. Questinon originally posted at [https://trailhead.salesforce.com/trailblazer-community/feed/0D54V00007T5wN2](https://trailhead.salesforce.com/trailblazer-community/feed/0D54V00007T5wN2)

## GitHub Action

A new Workflow was created to cache the dependencies: 
[cacheDependencies.yml](https://github.com/mvogelgesang/20231218_cacheGitHubActions/blob/main/.github/workflows/cacheDependencies.yml)

## Results

The result of the cached action reduces runtime by ~66%!

|Workflow Run|Cache Status|Duration|
|------------|------------|--------|
|[Caching SF CLI #13](https://github.com/mvogelgesang/20231218_cacheGitHubActions/actions/runs/7253534123)|Cache Miss|1m 47s|
|[Caching SF CLI #14](https://github.com/mvogelgesang/20231218_cacheGitHubActions/actions/runs/7253552656)|Cache Hit|35s|
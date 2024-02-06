# Event Store Helm Charts
This repository hosts the official Event Store Helm charts.

## Getting Started
1. Install Helm. Get the latest [Helm release](https://github.com/helm/helm#install).
2. Add the Event Store Helm repo.
    ```
    > helm repo add eventstore https://haimkortovich.github.io/EventStore.Charts
    > helm repo update
    ```
3. Install Event Store. See the chart's [README](./stable/eventstore/README.md) for instructions.

## Contributing to Event Store Charts
1. Fork the repo.
2. Make your changes. Make sure to follow [best practices](https://github.com/helm/helm/tree/master/docs/chart_best_practices).
3. Make sure tests pass.
4. Submit a pull request.

### Testing
On Windows (you will need [FAKE](https://fake.build/fake-gettingstarted.html)):
```
> fake build -f test/e2e-docker-desktop.fsx -t Test
```
On macOS:
```
> ./e2e-docker4mac.sh
```

### Releasing a new version

1. Bump the `version` in `stable/eventstore/Chart.yaml`
2. Release a new version: 
```bash
./release
```
> The `release` script packages the chart and updates the index.yaml accordingly 

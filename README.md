# PaC CheckRun Application Setup

Follow these steps to apply the PaC CheckRun:

1. Apply the application configuration:
    ```bash
    oc apply -f application-sample.yaml -n default
    ```

2. Apply the component configuration:
    ```bash
    oc apply -f component-sample.yaml -n default
    ```

3. Apply the integration test configuration:
    ```bash
    oc apply -f its.yaml -n default
    ```

4. Create the build configuration:
    ```bash
    oc create -f build.yaml -n default
    ```

## Expected Results:

After applying the PaC CheckRun, you should observe the following results:

1. The Build PipelineRun will be triggered and should succeed.

2. The Integration Test Scenario PipelineRun will be triggered and should succeed.

3. In the [GitHub Checks page](https://github.com/hacbs-integration-tests/Integration-pac-example/pull/1/checks), you should see an added CheckRun report for the Integration test.









> **Note:** For more detailed information and documentation, please refer to document [How to perform status reporting into Pull Requests?](https://docs.google.com/document/d/1DhmxW2LW4S7dwxFBP7GFYz3TFy2AmzxeUa6rEKMrb_8/edit#heading=h.66cora4dihms).
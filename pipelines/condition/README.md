# The flip-coin pipeline

The [flip-coin pipeline](https://github.com/kubeflow/pipelines/blob/master/samples/core/condition/condition.py)
is used to demonstrate the use of conditions. This pipeline is over-engineered
for what it does, but it demonstrate using `Condition`s in combination with
`Task`s and `PipelineResource`s.

To run this pipeline using `tkn`:

```
# Install tasks, conditions and pipeline
kubectl apply -f pipelines/condition/flip-coin.yaml

# Prepare the resources and apply them
kubectl apply -f pipelines/condition/resources.yaml


# Run the pipeline
tkn pipeline start flip-coin-condition-demo --resource=coin=coin-bucket --resource=random=random-bucket
```

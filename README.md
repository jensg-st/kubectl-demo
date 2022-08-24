# Add Pod

Adds a new pod based on the template used in `pod.yaml`. This YAML file is stored as workflow-scoped variable via the git file `add-pod.yaml.pod.yaml`.

```sh
echo '{"server": "https://10.100.6.10:6443",  "name": "hello" }' | direktiv-sync exec add-pod.yaml
```

# List Pods

Lists all pods with the label `server: http`.

```sh
echo '{"server": "https://10.100.6.10:6443" }' | direktiv-sync exec list-pods.yaml
```

# Pod Check

Checks if the pods with that name exists.

```sh
echo '{"server": "https://10.100.6.10:6443",  "name": "hello" }' | direktiv-sync exec exists-pod.yaml
```

# Delete Pod

Deletes a pod.

```sh
echo '{"server": "https://10.100.6.10:6443", "name": "hello" }' | direktiv-sync exec delete-pod.yaml
```

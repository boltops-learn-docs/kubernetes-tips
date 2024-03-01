<!-- note marker start -->
NOTE: This repo contains only the documentation for the private BoltsOps repo code.
Original file: https://github.com/boltops-learn/kubernetes-tips/blob/master/autocompletion.md
The docs are publish so they are available for interested subscribers.
For access to the source code, you can become a BoltOps subscriber.
See: https://learn.boltops.com

<!-- note marker end -->

# Kubernetes Auto-Completion

[![BoltOps Badge](https://img.boltops.com/boltops/badges/boltops-badge.png)](https://www.boltops.com)

## Examples

    kubectl get po[TAB]
    kubectl get pods[TAB]
    kubectl get pods web-[TAB]
    kubectl describe[TAB]
    kubectl delete[TAB]
    kubectl logs[TAB]

## Bash Shell

Add to your:

~/.bashrc

    source <(kubectl completion bash)

## Zsh Shell

Add this line to your:

~/.zshrc

    source <(kubectl completion zsh)

## Notes

* Resource-based auto-completion doesn't work unless cluster is working because it takes to the Cluster API.

## Video

[![Watch the video](https://uploads-learn.boltops.com/x1sq0g8mr0a4mj1689fr69rwkcgk)](https://learn.boltops.com/courses/kubernetes-tips/lessons/kubectl-autocompletion)

Note: Premium video content requires a subscription.

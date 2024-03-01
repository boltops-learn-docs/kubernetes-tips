<!-- note marker start -->
NOTE: This repo contains only the documentation for the private BoltsOps repo code.
Original file: https://github.com/boltops-learn/kubernetes-tips/blob/master/k-alias.md
The docs are publish so they are available for interested subscribers.
For access to the source code, you can become a BoltOps subscriber.
See: https://learn.boltops.com

<!-- note marker end -->

# k alias for kubectl

[![BoltOps Badge](https://img.boltops.com/boltops/badges/boltops-badge.png)](https://www.boltops.com)

Simple but one of my favorite tips.

## Bash Shell

~/.bashrc

    alias k=kubectl
    complete -F __start_kubectl k

## Zsh Shell

~/.zshrc

    autoload bashcompinit && bashcompinit # https://jessicadeen.com/fixed-az-completion10-command-not-found-complete/
    autoload -Uz compinit # https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/#optional-kubectl-configurations-and-plugins
    compinit
    source <(kubectl completion zsh)
    alias k=kubectl # helpful alias
    complete -F __start_kubectl k

## Video

[![Watch the video](https://uploads-learn.boltops.com/svn4tqfeb2dex6gi5868ltr9y5xy)](https://learn.boltops.com/courses/kubernetes-tips/lessons/k-alias-for-kubectl)

Note: Premium video content requires a subscription.

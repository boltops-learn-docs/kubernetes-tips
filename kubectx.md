<!-- note marker start -->
NOTE: This repo contains only the documentation for the private BoltsOps repo code.
Original file: https://github.com/boltops-learn/kubernetes-tips/blob/master/kubectx.md
The docs are publish so they are available for interested subscribers.
For access to the source code, you can become a BoltOps subscriber.
See: https://learn.boltops.com

<!-- note marker end -->

## kubectx vs kubectl

kubectx | kubectl | description
---|---|---
kubectx               | kubectl config get-contexts                     | list the contexts
kubectx NAME          | kubectl config use-context NAME                 | switch to context NAME
kubectx -             | kubectl config use-context PREVIOUS             | switch to the previous context
kubectx -c            | kubectl config current-context                  | show the current context name
kubectx NEW_NAME=NAME | kubectl config rename-context NAME NEW_NAME     | rename context NAME to NEW_NAME
kubectx NEW_NAME=.    | kubectl config rename-context $(kubectl config current-context) NEW_NAME | rename current-context to NEW_NAME
kubectx -d NAME       | kubectl config delete-context NAME              | delete context NAME ('.' for current-context) (this command won't delete the user/cluster entry that is used by the context)
kubectx -u            | kubectl config unset current-context            | unset the current context

## kubens vs kubectl

kubens | kubectl | description
---|---|---
kubens      | kubectl get ns                                                 | list the namespaces
kubens NAME | kubectl config set-context --current --namespace=NAME          | change the active namespace
kubens -    | kubectl config set-context --current --namespace=PREVIOUS      | switch to the previous namespace
kubens -c   | `kubectl config view --minify --output 'jsonpath={..namespace}'` | show the current namespace

## Video

[![Watch the video](https://uploads-learn.boltops.com/kd99poqgzrr715wzsr65inztdhx7)](https://learn.boltops.com/courses/kubernetes-tips/lessons/kubectx-and-kubens-vs-kubectl)

Note: Premium video content requires a subscription.

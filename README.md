# ingresssetup


in this repo we are going to settup ingress gateway for gke cluser'

Creating an external HTTP(S) load balancer
An external HTTP(S) load balancer provides one stable IP address that you can use to route requests to a variety of backend services. If you want a permanent IP address, you must reserve a global static external IP address.

In this exercise, you configure an external HTTP(S) load balancer to route requests to different backend services depending on the URL path. Requests that have the path / are routed to one backend service, and requests that have the path /v2 are routed to a different backend service.

Here's the big picture of the steps in this exercise:

Create a Deployment and expose it with a Service named hello-world-1.
Create a second Deployment and expose it with a Service named hello-world-2.
Create an Ingress that specifies rules for routing requests to one Service or the other, depending on the URL path in the request. When you create the Ingress, the GKE Ingress controller creates and configures an external HTTP(S) load balancer.
Test the external HTTP(S) load balancer.

1. Check if single namespace is not in use - pilot , mixer will ignore everything else.
2. Ensure that all services have "http-" in their port name
3. ingress port number must match service port number **and** the name must start with "http"
4. Check service, it must have valid endpoints
5. Create ingress resource for istio-system-ingress. This exposes mixer, pilot and prometheus
6. use curl -H "Host: istio-pilot" http://35.225.23.30/v1/routes/80/istio-ingress/ingress~~isistio-pilot-8c7b88d54-w782d-stio-system~istio-system.svc.cluster.cal
7. may also use  ./bin/istio-proxy-cfg to fetch info

8. Check direct mixer metrics by hitting mixer:42422/metrics
9. Check prometheus metrics


# Purpose

When `juju destroy-service` is called on a service, the service will be removed by juju, together with all its units
and relations. If this is the only service running, the machine on which the service is hosted will also be destroyed,
if possible. The machine will be destroyed if:
- it is not a state server
- it is not hosting any Juju managed containers

This is undesired at times. To prevent this from happening, deploy a stand-in service (like this one).
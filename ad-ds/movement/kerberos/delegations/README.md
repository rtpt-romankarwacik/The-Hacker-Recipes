# Delegations

The authentication protocol "Kerberos" features delegation capabilities described as follows. There are three types of Kerberos delegations

* **Unconstrained delegations (KUD)**: a service can impersonate users on any other service.
* **Constrained delegations (KCD)**: a service can impersonate users on a set of services
* **Resource based constrained delegations (RBCD)** : a set of services can impersonate users on a service

{% hint style="info" %}
With constrained and unconstrained delegations, the delegation attributes are set on the impersonating service (requires domain admin privileges) whereas with RBCD, these attributes are set on the target service account itself (requires lower privileges).
{% endhint %}

Kerberos delegations can be abused by attackers to obtain valuable assets and sometimes even domain admin privileges.

Some of the following parts allow to obtain modified or crafted Kerberos tickets. Once obtained, these tickets can be used with [Pass-the-Ticket](../pass-the-ticket.md).

{% content-ref url="unconstrained.md" %}
[unconstrained.md](unconstrained.md)
{% endcontent-ref %}

![](../../../../.gitbook/assets/Kerberos_delegations-unconstrained.drawio.png)

{% content-ref url="constrained.md" %}
[constrained.md](constrained.md)
{% endcontent-ref %}

![](../../../../.gitbook/assets/Kerberos_delegations-constrained.drawio.png)

{% content-ref url="rbcd.md" %}
[rbcd.md](rbcd.md)
{% endcontent-ref %}

![](../../../../.gitbook/assets/Kerberos_delegations-rbcd.drawio.png)
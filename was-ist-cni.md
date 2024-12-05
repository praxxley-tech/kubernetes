---
description: Ohne CNI kein Kubernetes -> Wie läuft der Verkehr über das Netzwerk
---

# Was ist CNI

<figure><img src=".gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

Worker nodes sollen die Arbeitslast der Kunden haben 1 - N

<figure><img src=".gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>



in den Pods laufen die C-RT (Control Runtime) und Kubelet -> Orchastriert die lokale Runtime und Kubelet spricht mit der Control plane node für die Orchestrierung

<figure><img src=".gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

Die CNI kümmert sich mit der Container Runtime das der Pod einen Port erhält.

<figure><img src=".gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

Diese können auch untereinander mit den Pods kommunizieren. Ohne das können die Nodes nicht miteinander kommunizieren.



Liste von CNI-Plugins

* flannel
* canal
* cilium
* weave net
* calico


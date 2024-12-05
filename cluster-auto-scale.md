# Cluster Auto-Scale

<figure><img src=".gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

**Cluster Autoscaler** in Kubernetes ist eine Funktion, die automatisch die Anzahl der Nodes in einem Cluster anpasst, basierend auf der Arbeitslast. Es stellt sicher, dass der Cluster genügend Ressourcen hat, um alle Pods auszuführen, und entfernt ungenutzte Nodes, um Kosten zu sparen.

1. **Aufwärts-Skalierung (Scale-Up)**:
   * Der Cluster Autoscaler fügt neue Nodes hinzu, wenn Pods nicht platziert werden können, weil der Cluster nicht genügend CPU, RAM oder andere Ressourcen hat.
2. **Abwärts-Skalierung (Scale-Down)**:
   * Der Cluster Autoscaler entfernt ungenutzte Nodes, wenn keine Pods auf einer Node laufen und genügend freie Ressourcen auf anderen Nodes verfügbar sind.
3. **Grenzen**:
   * Der Cluster Autoscaler arbeitet innerhalb der Grenzen des **Node-Pools** oder der Konfiguration deiner Cloud-Umgebung.

<figure><img src=".gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

# VPA

**Vertical Pod Autoscaler (VPA)** in Kubernetes ist ein Mechanismus, der die Ressourcenanforderungen von Pods dynamisch anpasst, um sicherzustellen, dass sie genügend CPU und Speicher haben, um effizient zu arbeiten, ohne die Ressourcen zu verschwenden. Im Gegensatz zum Horizontal Pod Autoscaler (HPA), der die Anzahl der Pods skaliert, passt VPA die **Ressourcenzuweisung einzelner Pods** an.

<figure><img src=".gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

**Wie funktioniert VPA?**

* **Zweck**: Optimierung der Ressourcennutzung durch automatische Anpassung der CPU- und Speicheranforderungen (`requests` und `limits`) eines Pods.
* **Arbeitsweise**:
  1. **Messung**: VPA überwacht kontinuierlich die Ressourcennutzung der Pods.
  2. **Empfehlung**: Basierend auf historischen und aktuellen Daten schlägt VPA neue `requests` und `limits` vor.
  3. **Anpassung**:
     * Bei **neuen Pods**: Die vorgeschlagenen Werte werden beim Erstellen des Pods angewendet.
     * Bei **laufenden Pods**: VPA startet Pods neu, um die neuen Ressourcenwerte anzuwenden (je nach Konfiguration).

```
// VPA-Controller
kubectl apply -f https://github.com/kubernetes/autoscaler/releases/latest/download/vertical-pod-autoscaler.yaml
```

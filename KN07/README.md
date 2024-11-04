Master Password:
admin1234

# bild (A):
![alt text]({9FD0838F-8119-46C2-9984-CC1FBB4DF861}.png)
Ein PaaS oder SaaS-Datenbankservice ist  besser, weil er weniger Verwaltungsaufwand erfordert, automatisch skaliert, hohe Verfügbarkeit und Sicherheit bietet und kosteneffizient ist. So kann ich mich auf die Entwicklung konzentrieren, ohne die Infrastruktur selbst betreiben und pflegen zu müssen.
# Screenshots (B):
![alt text]({78C8D2F6-82AA-4B7D-8F79-1467F81BF901}.png)
Für das Webserver-Setup habe ich eine internetzugängliche Umgebung gewählt. Der Plattformname "Corretto 21" bietet dabei eine stabile und AWS-optimierte Umgebung, die für die Anwendung Java-Kompatibilität sicherstellt.
![alt text]({9FF7FBF7-196F-4CA5-82A9-8832D125D9BF}.png)
Ich habe die Rolle "EMR_EC2_DefaultRole" genutzt, um der EC2-Instanz die nötigen Zugriffsrechte zu geben. Dadurch wird der sichere Zugriff auf weitere AWS-Dienste möglich und bleibt gleichzeitig unkompliziert.
![alt text]({C4F72CC6-9611-484A-A1E8-951B8088D77B}.png)
Eine isolierte VPC (Virtual Private Cloud) habe ich eingerichtet, um die Sicherheit der Netzwerkressourcen zu erhöhen. Die Aktivierung einer öffentlichen IP-Adresse erlaubt den Internetzugang, während die Subnetze eine sichere Verbindung innerhalb des Netzwerks gewährleisten.
![alt text]({98A3D4C8-6D97-4B0E-AC83-12337B94E52D}.png)
Bei der Instanzkonfiguration habe ich minimale und maximale EC2-Instanzen festgelegt, damit bei schwankendem Traffic automatisch zusätzliche Ressourcen bereitgestellt werden können.
![alt text]({2B833CB1-8F05-4F95-BC4B-FCCDECF6F7A5}.png)
Um den Wartungsaufwand zu verringern, habe ich automatische Updates aktiviert, die sicherstellen, dass alle Sicherheits- und Leistungsverbesserungen zeitnah umgesetzt werden. Das Logging ist momentan deaktiviert, kann jedoch bei Bedarf jederzeit aktiviert werden.
# (B2)
![alt text]({97E9DC62-E7E6-4BFF-9536-077C807D541E}.png)
![alt text]({55CFD546-11D0-4362-94C2-33CCEFC9DBB7}.png)
![alt text]({7CCAC9FC-68FE-4E2C-B750-9A5B4912BEAA}.png)
![alt text]({60BDF017-E838-41BB-BA8E-CB7DE3F21E94}.png)
![alt text]({7BB58BEA-18EC-48F6-B7FF-578A47794EC6}.png)
CloudFormation ist ein AWS-Tool zur Bereitstellung und Verwaltung ganzer Infrastrukturen als Code. Cloud-Init konfiguriert dagegen einzelne EC2-Instanzen beim Start. CloudFormation orchestriert die gesamte Umgebung, während Cloud-Init nur die Instanz-Initialisierung automatisiert.

**Vergleich der Auto-Scaling-Gruppe mit KN06:**

- **Kapazität:** Die aktuelle Auto-Scaling-Gruppe ist auf eine gewünschte Kapazität von 1 Instanz eingestellt, während KN06-AS mit 2 Instanzen konfiguriert ist. Dies deutet darauf hin, dass KN06-AS auf höhere oder stabilere Lasten ausgelegt ist.

- **Availability Zones:** Die ausgewählte Gruppe nutzt die Availability Zones `us-east-1a` und `us-east-1c`, wohingegen KN06-AS ausschließlich `us-east-1b` verwendet. Die Verteilung über mehrere Zonen erhöht die Ausfallsicherheit der ausgewählten Gruppe.

- **Instanztyp:** Beide Gruppen verwenden den Instanztyp `t3.micro`, was darauf hinweist, dass sie für leichte Workloads geeignet sind. Die unterschiedlichen Kapazitäten zeigen jedoch, dass sie an verschiedene Lastanforderungen angepasst wurden.


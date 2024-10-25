# Abgaben:
Ein Reverse Proxy leitet Anfragen von Nutzern an interne Server weiter, ohne diese direkt sichtbar zu machen. Er erhöht so die Sicherheit und kann den Datenverkehr besser verteilen.
![alt text](image.png)
![alt text](image-1.png)
![alt text](image-2.png)


# Vertikale Skalierung:
## before:
![alt text]({D43EB99C-39CB-4FE5-9B35-6325A3834A02}.png)
## after:
![alt text]({BC161203-D606-4B52-A37F-3A9DE922D5B2}.png)
### Laufender Betrieb?
Ja, das Ändern der Festplattengröße ist möglich, ohne die Instanz neu zu starten.

## before:
![alt text]({7CAE60EA-0254-4140-83FF-E8D1B2A75B40}.png)
## after:
![alt text]({297B354C-6678-4086-BB08-839C0112C3FA}.png)

### Laufender Betrieb?
Nein, das Ändern des Instanztyps ist nur im gestoppten Zustand möglich.

# Horizontale Skalierung
Wie müssten Sie den DNS konfigurieren, damit die Applikaiton unter URL app.tbz-m346.ch ist?
Damit das möglich ist, muss man einen A-record machen. Das würde die URL von der TBZ mit dem Load balancer DNS von mit verbinden.
Wie müssten Sie den DNS konfigurieren, damit dies funktioniert?
Um app.tbz-m346.ch zu konfigurieren, erstelle ich einen CNAME-Eintrag, der auf die Ziel-Domain (z.B. myapp.heroku.com) verweist. Falls eine IP-Adresse vorhanden ist, kann ich stattdessen einen A-Eintrag mit dieser IP verwenden. Diese Einträge ermöglichen es, dass die Domain auf die Anwendung verweist.
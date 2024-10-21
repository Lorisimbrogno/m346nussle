# alle zeilen ausführlich kommentiert:
#cloud-config
users:
  - name: ubuntu  # Definiert einen neuen Benutzer mit dem Namen 'ubuntu'
    sudo: ALL=(ALL) NOPASSWD:ALL  # Erlaubt dem Benutzer, sudo-Befehle ohne Passwort auszuführen
    groups: users, admin  # Fügt den Benutzer zu den Gruppen 'users' und 'admin' hinzu
    home: /home/ubuntu  # Setzt das Home-Verzeichnis des Benutzers auf '/home/ubuntu'
    shell: /bin/bash  # Legt die Standard-Shell des Benutzers auf '/bin/bash' fest
    ssh_authorized_keys:  # Hier wird der öffentliche SSH-Schlüssel hinzugefügt
      - ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC0WGP1EZykEtv5YGC9nMiPFW3U3DmZNzKFO5nEu6uozEHh4jLZzPNHSrfFTuQ2GnRDSt+XbOtTLdcj26+iPNiFoFha42aCIzYjt6V8Z+SQ9pzF4jPPzxwXfDdkEWylgoNnZ+4MG1lNFqa8aO7F62tX0Yj5khjC0Bs7Mb2cHLx1XZaxJV6qSaulDuBbLYe8QUZXkMc7wmob3PM0kflfolR3LE7LResIHWa4j4FL6r5cQmFlDU2BDPpKMFMGUfRSFiUtaWBNXFOWHQBC2+uKmuMPYP4vJC9sBgqMvPN/X2KyemqdMvdKXnCfrzadHuSSJYEzD64Cve5Zl9yVvY4AqyBD aws-key  # Öffentlicher SSH-Schlüssel für die Authentifizierung
ssh_pwauth: false  # Deaktiviert die Passwortauthentifizierung für SSH
disable_root: false  # Erlaubt den Zugriff auf den Root-Benutzer
package_update: true  # Aktualisiert die Paketliste beim Start der Instanz
packages:  # Liste der Pakete, die installiert werden sollen
  - curl  # Ein Kommandozeilen-Tool zum Übertragen von Daten mit URLs
  - wget  # Ein weiteres Kommandozeilen-Tool, um Inhalte von Webservern herunterzuladen

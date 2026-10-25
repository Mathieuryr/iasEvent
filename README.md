# iasEvent

1. [Télécharge cette archive](/Users/bebsulo/Documents/ChatGPT/RISE-IAS/outputs/controle_tango_exemples.zip) et décompresse-la sur l’autre PC.
2. Installe le gestionnaire officiel Python pour Windows. On utilisera Python 3.12, la version utilisée pour nos tests.
3. Ouvre le dossier décompressé controle_tango. Dans la barre d’adresse de l’Explorateur, tape powershell, puis Entrée.
   Exécute ces commandes une seule fois :
   py install 3.12
   py -3.12 -m venv .venv
   .\.venv\Scripts\python.exe -m pip install -r requirements.txt
   La commande d’installation de Python est documentée dans le guide officiel Windows.
4. Lance le contrôle sur les exemples fournis :
   .\.venv\Scripts\python.exe controle_tango.py --entree "examples_reels\audit_KAFKA.txt" --sortie "examples_reels\Kafka_audit_sortie.txt" --rapport "rapports_tango\exemple_reel.json"
   Puis ouvre le rapport :
   Start-Process ".\rapports_tango\exemple_reel.html"
Pour les utilisations suivantes, seule l’étape 4 est nécessaire. Remplace les chemins après --entree et --sortie pour comparer d’autres messages correspondant au même événement.

Les rapports HTML, CSV et JSON sont enregistrés dans rapports_tango. Le statut ECARTS_DETECTES signifie que le contrôle a trouvé des différences ; ce n’est pas un échec de lancement.

# SUNUPASS — App Console (version bureau)

Ce dépôt **ne contient aucune source**. Il sert uniquement de canal de distribution aux
installeurs de l'App Console SUNUPASS, publiés en *Releases*.

## Pourquoi un dépôt à part

Le code de la Console vit dans un dépôt **privé**. Or les fichiers attachés à une release d'un
dépôt privé exigent un jeton authentifié : un visiteur anonyme reçoit `404`. Les boutons de
téléchargement de l'écran *Paramètres* seraient donc tous en erreur.

Ce dépôt est également distinct de `sunupass-desktop`, qui distribue l'**Espace Exploitant** :
les deux applications pointent `/releases/latest/download/…`, et une seule release peut être
« latest ». Les réunir casserait silencieusement le lien de l'une le jour où l'autre publie.

## Télécharger

La dernière version : **[Releases](../../releases/latest)**

| Système | Fichier |
|---|---|
| Windows | `SUNUPASS-Console-win-x64.exe` |
| macOS Apple Silicon | `SUNUPASS-Console-mac-arm64.dmg` |
| macOS Intel | `SUNUPASS-Console-mac-x64.dmg` |
| Linux | `SUNUPASS-Console-linux-x86_64.AppImage` |

Ces noms ne portent **pas** de numéro de version : c'est ce qui rend l'adresse de téléchargement
stable d'une version à l'autre.

> Les binaires ne sont pas signés. Windows SmartScreen et macOS Gatekeeper afficheront un
> avertissement à la première installation.

## Ce que la version bureau apporte

Le **lecteur de cartes de comptoir**. Dans un navigateur, l'enrôlement d'une carte Pass oblige à
retaper son UID à la main ; en bureau, le lecteur PC/SC branché est reconnu et la carte se lit
d'elle-même.

## Publication

Automatique : un tag `vX.Y.Z` sur le dépôt de la Console déclenche la construction sur Windows,
macOS et Linux, puis la publication ici. Une release n'est rendue publique que si les quatre
installeurs ci-dessus sont présents — sinon elle reste en brouillon.

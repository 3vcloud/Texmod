ATTENTION : Vous utilisez ce programme � vous risque !
1) Si le programme plante, vous n'aurez probablement aucune aide des d�veloppeurs,
    mais vous pouvez envoyer le bogue sur http://code.google.com/p/texmod/issues/list
2) Les jeux peuvent d�tecter les modifications de uMod, vous prenez le risque de bannir
    votre compte en ligne !
3) C'est un projet open-source. Le code peut �tre r�cup�r�, modifi� et compil�
    par tout le monde. T�l�chargez Universal Modding Engine seulement sur des sources s�res !
    Ne t�l�charger pas et n'utiliser pas d'autres versions modifi�es de ce logiciel,
    par exemple des versions envoy�es par votre �quipe ou votre guilde !
    Le site officiel : http://code.google.com/p/texmod/downloads/list

Universal Modding Engine utilise le D3DX9_43.dll (32bit). En raison de la licence CLUF cette dll
ne peut pas �tre livr�e avec Universal Modding Engine . Si vous n'avez pas D3DX9_43.dll 
d'install� sur votre syst�me, Universal Modding Engine va vous afficher un message
au d�marrage du programme.


Que fait Universal Modding Engine (uMod) V1.0 ?

-Extraire et sauvegarder des textures d'un jeu DX9 (la texture d'origine peut se modifier)
-Extraire et sauvegarder toutes les textures d'un jeu DX9
-Charger des textures dans un jeu pour remplacer les textures d'origines
-Supporte les textures DDS
-Supporte les fichiers compress�s (ZIP) pour faire un MOD (modifier plusieurs textures � la fois)
-Supporte les fichiers de TexMod *.tpf

Toutes les options peuvent s'activer ou se d�sactiver, pendant que le jeu est lanc� !
Ainsi, vous pouvez rechercher une texture dans le jeu, l'enregistrer sur disque, la modifier,
la charger dans le jeu, �diter une autre texture, la charger dans le jeu, etc...,
Activer ou d�sactiver des MODs sans aucun red�marrage du jeu.

Remarque : Si vous cochez "Sauvegarder toutes les textures", les textures qui seront enregistr�es,
sont les textures charg�es dans le jeu apr�s le moment o� vous avez coch� la case.
Si vous activez cette option, pendant qu'une carte est charg�e, vous n'allez probablement rien enregistrer,
parce que toutes les textures sont d�j� charg�es. Changez de Carte ou rechargez-l�.

Les fichiers compress�s peuvent inclure le fichier "texmod.def" qui contient le hash et le nom du fichier.
Chaque ligne doit avoir le format "hash|filename.dds"
Si elle ne contient pas un "texmod.def" chaque fichier sera d�compress� et seuls les fichiers ayant
le format "*_hash.dds" seront utilis�s.
Le fichier zip peut inclure un fichier "Comment.txt". Le contenu sera affich� comme commentaire
dans l'interface graphique.

Si vous chargez des textures seules, elles doivent correspondre au format "*_hash.dds"


Comment Universal Modding Engine interagit avec les jeux ?

Universal Modding Engine intercepte la connexion entre le jeu et DirectX.
Il est n�cessaire, que Universal Modding Engine soit lanc� avant le jeu.

L'interface graphique de Universal Modding Engine est comme un serveur.
Un jeu correctement intercept� par Universal Modding Engine-dll se connectera au d�marrage sur le serveur.
L'interface graphique de Universal Modding Engine peut g�rer plusieurs jeux en m�me temps. Il sera
�galement traiter chaque jeu en tant que processus ind�pendant (si le m�me jeu
a �t� lanc� plus d'une fois).


Comment Universal Modding Engine fonctionne ?

Il y a trois fa�on pour que Universal Modding Engine intercepte la connexion � DirectX :
(Ne PAS utiliser plus d'une m�thode � la fois !)

1) Ajouter l'ex�cutable du jeu dans le menu "R�glages->Ajouter un jeu"
    Pour Steam, voir plus bas.
    
    Probl�mes connus : Guild Wars (Win XP)
    
2) Lancer le jeu directement via le menu uMod
    "R�glages->Lancer le jeu avec uMod" ou
	"R�glages->Lancer le jeu avec uMod (en ligne de commande)".
	Le jeu se lance directement.

3) Copier le d3d9.dll (depuis le r�pertoire de Universal Modding Engine) dans votre dossier de jeu.
    Certain jeu recherche les DLLs dans leur r�pertoire avant d'aller chercher les DLLs dans
	le dossier du syst�me.
    Cette m�thode ne fonctionne que sur certain jeu.
    ATTENTION : Ne jamais copier ce fichier DLL dans votre r�pertoire syst�me !!!
    
    Probl�mes connus : Guild Wars

Si vous avez choisi la premi�re ou la troisi�me m�thode, il vous suffit de lancer Universal Modding Engine
et de lancer le jeu s�par�ment. Ne PAS lancer le jeu via uMod.

Si le jeu se lance et tout fonctionne, un nouveau onglet va s'ouvrir directement dans uMod.
Dans cet onglet vous pouvez modifier le jeu. Appuyer sur "Mettre � jour" 
pour envoyer les changements au jeu. Vous pouvez sauvegarder vos param�tres actuels comme th�me.
Un th�me peut �tre lanc� par d�faut au d�marrage d'un jeu.

Pour charger une texture ou un mod, vous devez cocher la case du fichier. Si vous voulez d�charger un mod,
il faut simplement d�cocher la case et cliquer sur "Mettre � jour". 

En cliquant sur "Mettre � jour", seules les textures charg�es dans uMod seront misent � jour
(si une texture charg�e est supprim�e de la liste, cela va juste d�cocher la texture).
Cliquez sur "Mettre � jour (Recharger)" pour recharger les fichiers de texture sur le disque dur.
(Si vous venez de modifier une texture d�j� charg�e par exemple).

En raison du fait que plusieurs mods peuvent modifier la m�me texture, seuls le mod / la texture
du premier fichier de la liste est pris en compte pour la modification. L'action de ce mod
(c'est � dire le chargement ou le d�chargement) est effectu�e, ind�pendamment des autres mods.


Comment faire pour que Universal Modding Engine fonctionne avec Steam ?

Universal Modding Engine cherche le nom et le chemin du fichier binaire ex�cut�.
Ainsi vous ne devez pas ajouter Steam.exe mais plut�t le game.exe
exemple : C:\Steam\SteamApps\acoount_name\portal\hl2.exe
Si vous ne trouvez pas l'ex�cutable, il suffit de commencer le jeu et
d'utiliser "le Gestionnaire des t�ches" pour rechercher dans quel dossier il se trouve en
faisant un clique droit sur le nom de l'ex�cutable "Propri�t�s"->"Emplacement".
![img](https://img.shields.io/badge/EvilShell-v0.2.0-green) 
![img](https://img.shields.io/badge/Python-3.x-blue)
# EvilShell

EvilShell est un Reverse_TCP développé en Python 3. Il utilise les modules **os, socket, subprocess**.

# Qu'est-ce qu'un Reverse_TCP ?
Le reverse shell (shell inversé) - appelé aussi reverse tunnel (tunnel inversé) - est une technique informatique qui permet de rediriger sur un ordinateur local l'entrée et la sortie d'un shell vers un ordinateur distant, au travers d'un service capable d'interagir entre les deux ordinateurs.

*Source: Wikipédia*

![img](https://www.0x0ff.info/wp-content/uploads/2013/08/reverse_shell.png)

*Source: https://www.0x0ff.info/2013/reverse-shell*

# Capture d'écran
 ![img](https://www.zupimages.net/up/19/36/5617.png) 

# Méthode de propagation du Reverse_TCP avec PyInstaller
Pour que la victime ne soupçonne pas qu'il y a un Reverse_TCP sur son ordinateur, nous devons trouver un moyen de cacher l'ouverture du *CMD* au démarrage du programme. Pour cela, je vous propose d'utiliser la méthode avec l'outil PyInstaller qui permet de réaliser cette opération.

Tout d'abord, assurez-vous d'avoir édité le fichier "client.py" en changeant le port (int) et l'adresse (str) que vous voulez utiliser. Ensuite installez **PyInstaller** à l'aide de la commande :

	python3 -m pip install pyinstaller
 
Ensuite, pour diffuser le programme, tapez :

	pyinstaller -w -F client.py
 
L'option -w permet le camouflage de la console au démarrage. L'option -F permet d'obtenir un unique fichier, ce qui est plus facile pour sa propagation.

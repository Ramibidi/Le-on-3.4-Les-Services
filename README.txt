

php bin/console debug:container


Créer un fichier s’il n’existe pas (/create/{filename})
Écrire dans un fichier (/write/{filename}/{text})
Copier un fichier s’il existe (/copy/{from}/{to})
Supprimer un fichier (/delete/{filename})
Normalement, vos fichiers devront être créés dans le /web de votre application.
// Retoune un tableau associat
// Créé un fichier et retourne un tableau représentant tous les fichiers présents dans le meme dossier que lui après sa création
  public function createFile($filename)
// Supprime un fichier. Retoune True en cas de succès et false en cas d'échec. Si le fichier n'existait pas, c'est un echec.
  public function deleteFile($filename)
// Écrit dans un fichier à partir du $offset ième caractère.
  public function writeInFile($filename, $text, $offset = 0)
// Retourne le contenu d'un fichier
  public function readFile($filename)
Écrivez une action de controlleur pour chacune de ces fonctions:

/state
/create-file/{filename}
/delete-file/{filename}
/write-in-file/{filename}/{text}/{offset?}
/read-file/{filename}
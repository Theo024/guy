# Guy : le Git francophone

### Installation

Ajouter dans votre .bashrc ou votre .zshrc les lignes suivantes :

```sh
function do_git {
  local cmd=$1
  shift
  local extra=""
  if [[ "$cmd" == "tirer" ]]; then
    extra="pull"
  elif [[ "$cmd" == "pousser" ]]; then
    extra="push"
  elif [[ "$cmd" == "ajouter" ]]; then
    extra="add"
  elif [[ "$cmd" == "retirer" ]]; then
    extra="remove"
  elif [[ "$cmd" == "réinitialiser" ]]; then
    extra="reset"
  elif [[ "$cmd" == "commettre" ]]; then
    extra="commit"
  elif [[ "$cmd" == "vérifier" ]]; then
    extra="checkout"
  elif [[ "$cmd" == "situation" ]]; then
    extra="status"
  elif [[ "$cmd" == "initialiser" ]]; then
    extra="init"
  elif [[ "$cmd" == "branche" ]]; then
    extra="branch"
  elif [[ "$cmd" == "fusionner" ]]; then
    extra="merge"
  fi
  git $extra $@
}

alias guy='do_git'
```

Il suffit alors de relancer votre terminal ou entrer la commande suivante :

* Pour ```bash```
  ```sh
  $ source ~/.bahsrc
  ```

* Pour ```zsh```
  ```sh
  $ source ~/.zshrc
  ```

### Utilisation

L'utilisation de ```guy``` est similaire à celle de ```git```.

| git | guy |
| --- | --- |
| init | initialiser |
| status | situation |
| checkout | vérifier |
| branch | branche |
| merge | fusionner |
| add | ajouter |
| remove | retirer |
| reset | réinitialiser |
| commit | commettre |
| pull | tirer |
| push | pousser |

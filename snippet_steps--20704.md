# my_snippet--20704


# install doodba copier template in new directory
copier copy gh:Tecnativa/doodba-copier-template d13.0


# cd
cd d13.0/


# ¿base?
invoke install -m base


# add repos
nano odoo/custom/src/addons.yaml


# repos
- `l10n-spain: ["*"]`
- `mis-builder: ["*"]`


# invoke
- invoke git-aggregate
- invoke develop
- invoke start (¿ docker-compose up-d ?)
- ~invoke install -m base~
- ~invoke install -m sale_management~
- inv install -m base,sale_management
- inv install --core (core modules)
- inv install --private (private modules)


# invoke commands
- can be ckecked from "tasks.py" file
- search for "def install" and you'll find install commands


# add pyOpenSSL, if needed, to pip.txt (odoo/custom/dependencies)
nano pip.txt


# launch invoke arguments
- develop 
- img-pull 
- img-build 
- --pull 
- git-aggregate 
- resetdb 
- start


# Notes:
If changing Odoo version only, you can type: `copier -f -d odoo_version=THE_VERSION_OF_ODOO copy gh:Tecnativa/doodba-copier-template NEW_BINDER && cd NEW_BINDER`
For example: `copier -f -d odoo_version=13.0 copy gh:Tecnativa/doodba-copier-template dct-13 && cd dct-13`

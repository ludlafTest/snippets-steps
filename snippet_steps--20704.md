# my_snippet--20704


## install doodba copier template in new directory
copier copy gh:Tecnativa/doodba-copier-template d13.0


## cd
cd d13.0/


## add repos
nano odoo/custom/src/addons.yaml


# l10n-spain: ["*"]
# mis-builder: ["*"]


## invoke
invoke git-aggregate
invoke develop
invoke install -m base
invoke install -m sale_management


## add pyOpenSSL to pip.txt (odoo/custom/dependencies)
nano pip.txt


## launch invoke arguments
invoke develop img-pull img-build --pull git-aggregate resetdb start

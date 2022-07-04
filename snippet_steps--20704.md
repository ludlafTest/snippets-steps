## my_snippet--20704
# ~mkdir v13.0 (choose Odoo version)~ \ ~mkdir v13.0~ \ ~cd v13.0~


# ---
# install doodba copier template in new directory
copier copy gh:Tecnativa/doodba-copier-template d13.0


# ---
# cd
cd d13.0/


# ---
# add repos
nano odoo/custom/src/addons.yaml
l10n-spain: ["*"]
mis-builder: ["*"]


# ---
# invoke
invoke git-aggregate
invoke develop
invoke install -m base
invoke install -m sale_management


# ---
# ignore from here downwards


---
#####
# ---
# add info to addons.yaml (odoo/custom/src/addons.yaml)
account-financial-reporting: ["*"]
account-financial-tools: ["*"]
account-invoice-reporting: ["*"]
account-invoicing: ["*"]
apps-store: ["*"]
bank-payment: ["*"]
calendar: ["*"]
commission: ["*"]
community-data-files: ["*"]
contract: ["*"]
credit-control: ["*"]
crm: ["*"]
data-protection: ["*"]
dms: ["*"]
e-commerce: ["*"]
event: ["*"]
hr-holidays: ["*"]
hr: ["*"]
knowledge: ["*"]
l10n-spain: ["*"]
mis-builder: ["*"]
multi-company: ["*"]
oca-custom: ["*"]
partner-contact: ["*"]
product-attribute: ["*"]
product-pack: ["*"]
project: ["*"]
purchase-workflow: ["*"]
queue: ["*"]
report-print-send: ["*"]
reporting-engine: ["*"]
rest-framework: ["*"]
rma: ["*"]
sale-workflow: ["*"]
server-auth: ["*"]
server-backend: ["*"]
server-brand: ["*"]
server-tools: ["*"]
server-ux: ["*"]
social: ["*"]
stock-logistics-barcode: ["*"]
stock-logistics-warehouse: ["*"]
stock-logistics-workflow: ["*"]
survey: ["*"]
timesheet: ["*"]
web: ["*"]
website: ["*"]~


# ---
# add pyOpenSSL to pip.txt (odoo/custom/dependencies)
nano pip.txt


# ---
# launch invoke commands (invoke develop img-pull img-build --pull git-aggregate
# resetdb start)
invoke develop img-pull img-build --pull git-aggregate

# mkdir v13.0 (choose Odoo version)
mkdir v13.0
cd v13.0


# ---
# install doodba copier template in present directory
copier copy gh:Tecnativa/doodba-copier-template .


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
website: ["*"]


# ---
# add pyOpenSSL to pip.txt (odoo/custom/dependencies)
nano pip.txt


# ---
# launch invoke commands (invoke develop img-pull img-build --pull git-aggregate
# resetdb start)
invoke develop img-pull img-build --pull git-aggregate



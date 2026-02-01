# Mini-projet Azure AZ-104 – Infrastructure as Code (ARM)

## 🎯 Objectif
Déployer automatiquement un **Storage Account Azure** à l’aide d’un **template ARM**, en respectant les bonnes pratiques de sécurité, d’automatisation et de gestion des coûts.

Ce projet illustre un usage réel du cloud Azure conforme au niveau **Administrateur Azure (AZ-104)**.

---

## 🛠️ Technologies utilisées
- Microsoft Azure
- Azure Resource Manager (ARM)
- Azure Cloud Shell (PowerShell)
- Git & GitHub
- Infrastructure as Code (IaC)

---

## 📦 Ressources déployées
- **Storage Account (StorageV2)**
  - SKU : Standard_LRS
  - Région : France Central
  - HTTPS uniquement activé
  - Accès Hot Tier

---

## 🚀 Déploiement automatisé
```powershell
New-AzResourceGroupDeployment `
  -Name deploy-az104-mini `
  -ResourceGroupName rg-az104-mini `
  -TemplateFile azuredeploy.json `
  -TemplateParameterFile azuredeploy.parameters.json

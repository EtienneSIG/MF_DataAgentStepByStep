# Microsoft Fabric - Démos Customer 360 & ESG

**14 scénarios de démonstration** illustrant les capacités de Microsoft Fabric :
- OneLake + Shortcuts
- AI Shortcut Transformations (texte → données structurées)
- Fabric Data Agent (questions en langage naturel)
- Power BI Semantic Models (métriques métier)

---

## 📊 Tableau Récapitulatif des Scénarios

| # | Scénario | Cas d'Usage | Volumes Données | Métriques Clés | Persona | Documentation |
|---|----------|-------------|-----------------|----------------|---------|---------------|
| **1** | **📞 Call Center** | Customer 360 + analyse appels | • 1K clients<br>• 15K commandes<br>• 2K appels<br>• 15 agents | • CSAT (70-80%)<br>• FCR (~70%)<br>• AHT<br>• Repeat Call Rate | Call Center Analyst | [📂 Dossier](https://github.com/EtienneSIG/MF_CallCenter) |
| **2** | **🏭 Production** | Monitoring production + maintenance | • 3 plants, 6 lines<br>• 100 assets<br>• 4K batches<br>• 300 work orders | • OEE (75-80%)<br>• MTTR (100-120min)<br>• MTBF<br>• Downtime Cost | Production & Maintenance Analyst | [📂 Dossier](https://github.com/EtienneSIG/MF_SupplyMaintenance)|
| **3** | **📧 Marketing** | Attribution marketing + ROI | • 10K customers<br>• 60 campaigns<br>• 150K sends<br>• 50K orders | • Campaign ROI (+100-500%)<br>• Open Rate (~22%)<br>• CTR, Conversion<br>• CLV | Marketing & CRM Analyst | [📂 Dossier](https://github.com/EtienneSIG/MF_MarketingCampaign)|
| **4** | **💰 Finance** | P&L + Budget vs Actual | • Actuals, Budget<br>• Invoices, Payments<br>• Cost Centers | • Gross Margin (40-45%)<br>• EBITDA, Net Income<br>• Budget Variance<br>• DSO (30-45 days) | Finance Controller | [📂 Dossier](https://github.com/EtienneSIG/MF_Finance)|
| **5** | **🌱 ESG** | Carbon footprint + sustainability | • Scope 1/2/3<br>• 10 sites, 5 ans<br>• 100 suppliers<br>• Audits | • Carbon Footprint (CO2e)<br>• Carbon Intensity<br>• Renewable Energy %<br>• Supplier Risk | ESG & Sustainability Manager | [📂 Dossier](https://github.com/EtienneSIG/MF_ESG) |
| **6** | **💻 IT Ops & FinOps** | Cloud cost optimization + performance | • 500 resources<br>• 5K users<br>• 500K cost events<br>• 300 incidents | • Cost per Resource<br>• WAU (Weekly Active Users)<br>• MTTR Incidents<br>• Anomaly Detection | Cloud FinOps Analyst | [📂 Dossier](https://github.com/EtienneSIG/MF_ITOps) |
| **7** | **📱 Product Analytics** | Product usage + churn prediction | • 500 accounts<br>• 5K users<br>• 50 features<br>• 500K usage events<br>• 1K feedbacks | • Churn Rate (50% Pro)<br>• MRR (~$300K)<br>• DAU/MAU Stickiness<br>• Feature Adoption<br>• NPS Score | Product Analyst | [📂 Dossier](https://github.com/EtienneSIG/MF_ProductUsage) |
| **8** | **⚖️ Risk & Compliance** | Risk management + audit compliance | • 150 controls<br>• 3K executions<br>• 200 incidents<br>• 100 vendors<br>• 100 audit reports | • Compliance Rate (~90%)<br>• MTTR by Severity<br>• Vendor Risk Score<br>• Incident Trends | Risk & Compliance Manager | [📂 Dossier](https://github.com/EtienneSIG//MF_RiskComplianceAudit) |
| **9** | **🔬 R&D & Quality** | Product testing + quality analytics | • 50 designs<br>• 100 test campaigns<br>• 5K test results<br>• 300 defects<br>• 250 field returns | • First Pass Yield (95%)<br>• Field Return Rate (<2%)<br>• Test Escape Rate<br>• Defect Density | VP Engineering & Quality | [📂 Dossier](https://github.com/EtienneSIG/)/MF_R-D) |
| **10** | **👥 HR Analytics** | Employee lifecycle (hire to retire) | • 500 employees<br>• 4K events<br>• 2.5K trainings<br>• 200+ rapports | • Attrition (12-13%)<br>• Promotion Rate (10%)<br>• Training/FTE (42h)<br>• Mobility (14-15%) | HR Analytics AI Assistant | [📂 Dossier](https://github.com/EtienneSIG/MF_HR)|

---

## 🎯 Points Forts par Scénario

| Scénario | Fonctionnalités Clés |
|----------|----------------------|
| **Call Center** | • AI Transformations sur transcripts d'appels<br>• Analyse sentiment + PII redaction<br>• Customer 360 avec historique commandes |
| **Production** | • OEE monitoring temps réel<br>• Maintenance prédictive<br>• Cost analysis (downtime, quality) |
| **Marketing** | • Attribution marketing multi-touch<br>• ROI campaigns avec drill-down<br>• CLV prediction + segmentation |
| **Finance** | • Budget variance analysis<br>• Cash flow forecasting<br>• P&L drill-down par cost center |
| **ESG** | • Scope 1/2/3 emissions tracking<br>• Supplier risk scoring<br>• Carbon intensity KPIs + targets |
| **IT Ops & FinOps** | • Multi-cloud cost aggregation (Azure, AWS, GCP)<br>• Anomaly detection sur coûts<br>• Incident correlation avec coûts<br>• User activity monitoring (WAU, engagement) |
| **Product Analytics** | • Churn prediction par plan (Free/Pro/Enterprise)<br>• AI sentiment analysis sur feedbacks utilisateurs<br>• Feature adoption funnel analysis<br>• NPS tracking + thèmes extraits (AI Transformations) |
| **Risk & Compliance** | • Multi-framework compliance (SOX, GDPR, ISO27001, PCI-DSS)<br>• AI extraction des findings d'audit<br>• Third-party risk scoring (vendors)<br>• Incident correlation avec contrôles échoués |
| **R&D & Quality** | • Test effectiveness analysis (DVT, PVT, Qualification)<br>• AI extraction engineering notes (root causes, design changes)<br>• Correlation test failures ↔ field returns<br>• Predictive quality analytics (FPY, defect density) |
| **HR Analytics** | • SCD Type 2 employee tracking<br>• AI exit interview analysis<br>• Predictive attrition + retention ROI<br>• Cohorte analysis (tenure, promotions) |
---

## 🧪 Tests Recommandés

Pour chaque scénario :

1. ✅ **Validation schéma** : `python validate_schema.py` → exit code 0
2. ✅ **Relations Semantic Model** : Toutes les relations créées, cardinalités correctes
3. ✅ **Mesures DAX** : Pas de BLANK() inattendu, valeurs cohérentes
4. ✅ **Data Agent** : 15-20 questions test (voir `data_agent_examples.md`)

---

## 🔗 Ressources

- [Documentation Microsoft Fabric](https://learn.microsoft.com/en-us/fabric/)
- [GHG Protocol (ESG)](https://ghgprotocol.org/)
- [OEE.com (Production)](https://www.oee.com/)
- [DAX Guide](https://dax.guide/)

---

## 📞 Support

Pour questions sur les scénarios :
- Consulter les `README.md` et `CORRECTIONS_SCENARIO.md` de chaque scénario
- Vérifier les `AGENTS.md` pour conventions de développement

**Version** : Janvier 2026 - Corrections post-demo appliquées

---

*Démonstrations Microsoft Fabric - Customer 360, Production, Marketing, Finance & ESG*






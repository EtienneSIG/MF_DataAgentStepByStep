# Microsoft Fabric - Démos Customer 360 & ESG

**10 scénarios de démonstration** illustrant les capacités de Microsoft Fabric :
- OneLake + Shortcuts
- AI Shortcut Transformations (texte → données structurées)
- Fabric Data Agent (questions en langage naturel)
- Power BI Semantic Models (métriques métier)

---

## � Tableau Récapitulatif des Scénarios

| # | Scénario | Cas d'Usage | Volumes Données | Métriques Clés | Persona | Documentation |
|---|----------|-------------|-----------------|----------------|---------|---------------|
| **1** | **📞 Call Center** | Customer 360 + analyse appels | • 1K clients<br>• 15K commandes<br>• 2K appels<br>• 15 agents | • CSAT (70-80%)<br>• FCR (~70%)<br>• AHT<br>• Repeat Call Rate | Call Center Analyst | [📂 Dossier](https://github.com/EtienneSIG/MF_CallCenter) |
| **2** | **🏭 Production** | Monitoring production + maintenance | • 3 plants, 6 lines<br>• 100 assets<br>• 4K batches<br>• 300 work orders | • OEE (75-80%)<br>• MTTR (100-120min)<br>• MTBF<br>• Downtime Cost | Production & Maintenance Analyst | [📂 Dossier](https://github.com/EtienneSIG/MF_SupplyMaintenance)|
| **3** | **📧 Marketing** | Attribution marketing + ROI | • 10K customers<br>• 60 campaigns<br>• 150K sends<br>• 50K orders | • Campaign ROI (+100-500%)<br>• Open Rate (~22%)<br>• CTR, Conversion<br>• CLV | Marketing & CRM Analyst | [📂 Dossier](https://github.com/EtienneSIG/MF_MarketingCampaign)|
| **4** | **💰 Finance** | P&L + Budget vs Actual | • Actuals, Budget<br>• Invoices, Payments<br>• Cost Centers | • Gross Margin (40-45%)<br>• EBITDA, Net Income<br>• Budget Variance<br>• DSO (30-45 days) | Finance Controller | [📂 Dossier](https://github.com/EtienneSIG/MF_Finance)|
| **5** | **🌱 ESG** | Carbon footprint + sustainability | • Scope 1/2/3<br>• 10 sites, 5 ans<br>• 100 suppliers<br>• Audits | • Carbon Footprint (CO2e)<br>• Carbon Intensity<br>• Renewable Energy %<br>• Supplier Risk | ESG & Sustainability Manager | [📂 Dossier](https://github.com/EtienneSIG/MF_ESG) |
| **10** | **👥 HR Analytics** | Employee lifecycle (hire to retire) | • 500 employees<br>• 4K events<br>• 2.5K trainings<br>• 200+ rapports | • Attrition (12-13%)<br>• Promotion Rate (10%)<br>• Training/FTE (42h)<br>• Mobility (14-15%) | HR Analytics AI Assistant | [📂 Dossier](https://github.com/EtienneSIG/MF_HR))|

---

## 🎯 Points Forts par Scénario

| Scénario | Fonctionnalités Clés |
|----------|----------------------|
| **Call Center** | • AI Transformations sur transcripts d'appels<br>• Analyse sentiment + PII redaction<br>• Customer 360 avec historique commandes |
| **Production** | • OEE monitoring temps réel<br>• Maintenance prédictive<br>• Cost analysis (downtime, quality) |
| **Marketing** | • Attribution marketing multi-touch<br>• ROI campaigns avec drill-down<br>• CLV prediction + segmentation |
| **Finance** | • Budget variance analysis<br>• Cash flow forecasting<br>• P&L drill-down par cost center |
| **ESG** | • Scope 1/2/3 emissions tracking<br>• Supplier risk scoring<br>• Carbon intensity KPIs + targets |
| **HR Analytics** | • SCD Type 2 employee tracking<br>• AI exit interview analysis<br>• Predictive attrition + retention ROI<br>• Cohorte analysis (tenure, promotions) |

---

## 🛠️ Corrections Appliquées (Tous Scénarios)

**Données** :
- **Commerce** : 1 000 clients, 800 produits, 15 000 commandes
- **Call Center** : 2 000 appels, 15 agents, transcripts texte (AI Transformations)

**Métriques clés** :
- CSAT (Customer Satisfaction Score)
- FCR (First Call Resolution)
- AHT (Average Handle Time)
- Repeat Call Rate

**Liens** :
- 📂 [Dossier Scenario 1](../Scenario%201-%20Call%20center/)
- 📄 [README](../Scenario%201-%20Call%20center/README.md)
- 🔧 [Corrections & Fixes](../Scenario%201-%20Call%20center/docs/CORRECTIONS_SCENARIO.md)
- 📊 [Mesures DAX](../Scenario%201-%20Call%20center/docs/dax_measures.md)
- 🧪 [Validation Script](../Scenario%201-%20Call%20center/src/validate_schema.py)
- 🤖 [Data Agent Instructions](../Scenario%201-%20Call%20center/docs/data_agent_instructions_clean.md)

**Persona Data Agent** : Call Center Analyst

---

## 🏭 Scenario 2 - Production & Maintenance

**Cas d'usage** : Monitoring production automobile + maintenance prédictive

**Données** :
- **Production** : 3 plants, 6 lines, 100 assets, 4 000 batches
- **Maintenance** : 300 work orders, rapports texte (AI Transformations)

**Métriques clés** :
- OEE (Overall Equipment Effectiveness)
- MTTR (Mean Time To Repair)
- MTBF (Mean Time Between Failures)
- Downtime Cost, Quality Cost

**Liens** :
- 📂 [Dossier Scenario 2](../Scenario%202-%20Maintenance%20supply/)
- 📄 [README](../Scenario%202-%20Maintenance%20supply/README.md)
- 🔧 [Corrections & Fixes](../Scenario%202-%20Maintenance%20supply/docs/CORRECTIONS_SCENARIO.md)
- 📊 [Mesures DAX](../Scenario%202-%20Maintenance%20supply/docs/dax_measures.md)
- 🧪 [Validation Script](../Scenario%202-%20Maintenance%20supply/src/validate_schema.py)
- 🤖 [Data Agent Instructions](../Scenario%202-%20Maintenance%20supply/docs/data_agent_instructions_clean.md)

**Persona Data Agent** : Production & Maintenance Analyst

---

## 📧 Scenario 3 - Marketing Campaigns

**Cas d'usage** : Customer 360 avec attribution marketing

**Données** :
- **CRM** : 10 000 customers, 50 segments, 200 000 interactions
- **Marketing** : 60 campaigns, 150 000 sends, 35 000 events (open, click, bounce)
- **Commerce** : 800 products, 50 000 orders
- **Texte** : 20 000 customer notes, 60 email bodies (AI Transformations)

**Métriques clés** :
- Campaign ROI (Return On Investment)
- Open Rate, CTR (Click-Through Rate), Conversion Rate
- CLV (Customer Lifetime Value)
- Attribution Last-Touch (14 jours)

**Liens** :
- 📂 [Dossier Scenario 3](../Scenario%203%20-%20Marketing%20Campagn/)
- 📄 [README](../Scenario%203%20-%20Marketing%20Campagn/README.md)
- 🔧 [Corrections & Fixes](../Scenario%203%20-%20Marketing%20Campagn/docs/CORRECTIONS_SCENARIO.md)
- 📊 [Mesures DAX](../Scenario%203%20-%20Marketing%20Campagn/docs/dax_measures.md)
- 🧪 [Validation Script](../Scenario%203%20-%20Marketing%20Campagn/src/validate_schema.py)
- 🤖 [Data Agent Instructions](../Scenario%203%20-%20Marketing%20Campagn/docs/data_agent_instructions_clean.md)
- 📋 [Summary Corrections](../Scenario%203%20-%20Marketing%20Campagn/docs/SUMMARY.md)
- 🚀 [Quickstart Guide](../Scenario%203%20-%20Marketing%20Campagn/QUICKSTART_CORRECTIONS.md)

**Persona Data Agent** : Marketing & CRM Analyst

---

## 💰 Scenario 4 - Finance Performance Management

**Cas d'usage** : Analyse financière P&L + Budget vs Actual

**Données** :
- **Finance** : actuals, budget, invoices, payments
- **Dimensions** : accounts, cost centers, customers

**Métriques clés** :
- Gross Margin %, EBITDA, Net Income
- Budget Variance (Amount & %)
- DSO (Days Sales Outstanding)
- Accounts Receivable, Collection Rate

**Liens** :
- 📂 [Dossier Scenario 4](../Scenario%204%20-%20Finance/)
- 📄 [README](../Scenario%204%20-%20Finance/README.md)
- 🔧 [Corrections & Fixes](../Scenario%204%20-%20Finance/docs/CORRECTIONS_SCENARIO.md)
- 📊 [Mesures DAX](../Scenario%204%20-%20Finance/docs/dax_measures.md)
- 🧪 [Validation Script](../Scenario%204%20-%20Finance/src/validate_schema.py)
- 🤖 [Data Agent Instructions](../Scenario%204%20-%20Finance/docs/data_agent_instructions_clean.md)

**Persona Data Agent** : Finance Controller

---

## 🌱 Scenario 5 - ESG & Carbon Analytics

**Cas d'usage** : Suivi performance ESG + carbon footprint

**Données** :
- **Emissions** : Scope 1/2/3, 10 sites, 5 ans historique
- **Energy** : consommation, % renewable
- **Supply Chain** : 100 suppliers, risk assessment
- **Governance** : audits, compliance reports (AI Transformations)

**Métriques clés** :
- Total Carbon Footprint (tonnes CO2e)
- Carbon Intensity (kg CO2e/unité)
- Target Achievement %, Reduction from Baseline
- Renewable Energy %, Supplier Risk Exposure

**Liens** :
- 📂 [Dossier Scenario 5](../Scenario%205%20-%20ESG/)
- 📄 [README](../Scenario%205%20-%20ESG/README.md)
- 🔧 [Corrections & Fixes](../Scenario%205%20-%20ESG/docs/CORRECTIONS_SCENARIO.md)
- 📊 [Mesures DAX](../Scenario%205%20-%20ESG/docs/dax_measures.md)
- 🧪 [Validation Script](../Scenario%205%20-%20ESG/src/validate_schema.py)
- 🤖 [Data Agent Instructions](../Scenario%205%20-%20ESG/docs/data_agent_instructions_clean.md)

**Persona Data Agent** : ESG & Sustainability Manager

---

## � Scenario 10 - HR Employee Lifecycle Analytics

**Cas d'usage** : Analyse complète du cycle de vie des employés

**Données** :
- **HR Core** : ~500 employees (actifs + historique), 12 departments, 45 positions
- **Lifecycle Events** : 4 000 événements (embauches, promotions, mutations, départs)
- **Compensation** : 1 500 historiques de salaires
- **Training** : 2 500 formations (42h/FTE moyenne)
- **Absences** : 3 000 enregistrements (congés, maladie)
- **HR Cases** : 150 cas (conflits, disciplinaires, réclamations)
- **Rapports Texte** : 200+ rapports (exit interviews, performance reviews, AI Transformations)

**Métriques clés** :
- Headcount & Headcount Growth Rate
- Attrition Rate (global, voluntary, involuntary)
- Promotion Rate, Internal Mobility Rate
- Training Hours per FTE, Training ROI
- Avg Time to Promotion, Avg Case Resolution Time
- Absence Rate per FTE

**Architecture** :
- **Medallion** : Bronze (8 CSV raw) → Silver (4 dimensions SCD Type 2) → Gold (6 fact tables)
- **AI Transformations** : PII redaction + text summarization sur rapports RH
- **Star Schema** : dim_employee (SCD2), dim_department, dim_position, dim_date + 6 fact tables

**Liens** :
- 📂 [Dossier Scenario 10](./Scenario%2010%20-%20HR/)
- 📄 [README](./Scenario%2010%20-%20HR/README.md)
- 📊 [Schéma Complet](./Scenario%2010%20-%20HR/docs/schema.md)
- 🎯 [Mesures DAX](./Scenario%2010%20-%20HR/docs/dax_measures.md)
- 🧪 [Validation Script](./Scenario%2010%20-%20HR/src/validate_schema.py)
- 🤖 [Data Agent Instructions](./Scenario%2010%20-%20HR/docs/data_agent_instructions.md)
- 📚 [20 Exemples Questions/Réponses](./Scenario%2010%20-%20HR/docs/data_agent_examples.md)
- 🎤 [15 Questions Démo "Wow"](./Scenario%2010%20-%20HR/docs/questions_demo.md)
- 🎬 [Démo Story Narrative](./Scenario%2010%20-%20HR/docs/demo_story.md)
- ⚙️ [Guide Setup Fabric](./Scenario%2010%20-%20HR/docs/fabric_setup.md)

**Persona Data Agent** : HR Analytics AI Assistant

**Points forts** :
- ✨ SCD Type 2 sur dim_employee (tracking historique complet)
- ✨ AI redaction PII (RGPD-compliant) + summarization des exit interviews
- ✨ Analyse prédictive : risque de départ, segmentation rétention, ROI budgets
- ✨ Cohorte analysis : attrition par année d'embauche, progression de carrière
- ✨ 30+ mesures DAX : Attrition, Promotion Rate, Training ROI, Mobility, etc.

---

## �🛠️ Corrections Appliquées (Tous Scénarios)

Suite aux retours de démo, **3 problèmes identifiés et corrigés** :

### ❌ Problème 1 : AI Shortcut Transformations KO

**Cause** : Fichiers TXT avec headers custom non parsés par Fabric

**Solution recommandée** : **Option C** (CSV avec colonne content)
- Générer CSV avec colonnes structurées (id, date, content)
- Appliquer AI Skills (PII detection, sentiment, extraction) sur colonne `content`
- Évite parsing headers custom, garantit compatibilité Fabric

**Impact** : Tous scénarios avec texte (1, 2, 3, 5)

### ❌ Problème 2 : DAX Queries avec Erreurs de Nommage

**Cause** : Colonnes mal nommées ou absentes dans CSV

**Solution** :
- Scripts `validate_schema.py` créés pour chaque scénario
- Validation automatique avant déploiement Fabric
- Exemples : `attributed_campaign_id` absent, `event_type` valeurs incorrectes

**Impact** : Tous scénarios

### ❌ Problème 3 : Data Agent Instructions Trop Longues

**Cause** : Instructions 350+ lignes avec emojis (non professionnel)

**Solution** :
- Fichiers `data_agent_instructions_clean.md` créés (250 lignes max)
- Format markdown strict, sans emojis
- Persona adapté par scénario

**Impact** : Tous scénarios

---

## 📋 Fichiers de Corrections (Chaque Scénario)

Chaque scénario contient maintenant :

| Fichier | Description |
|---------|-------------|
| `docs/CORRECTIONS_SCENARIO.md` | Analyse détaillée des 3 problèmes + solutions |
| `docs/data_agent_instructions_clean.md` | Instructions Data Agent (version propre) |
| `docs/dax_measures.md` | 30-50 mesures DAX testées et validées |
| `src/validate_schema.py` | Script Python de validation schéma |

**Scénario 3 uniquement** (référence complète) :
- `docs/SUMMARY.md` : Guide complet des corrections
- `QUICKSTART_CORRECTIONS.md` : Déploiement rapide (10 min)

---

## 🚀 Déploiement Rapide (Quickstart)

### 1. Valider le Schéma

```powershell
# Pour chaque scénario
cd "Scenario X - Name/src"
python validate_schema.py

# Output attendu : "✅ Schéma validé avec succès"
```

### 2. Créer Lakehouse + Shortcuts

- Créer Lakehouse dans Fabric
- Ajouter Shortcuts vers dossiers CSV :
  - `commerce/` (si applicable)
  - `crm/` (si applicable)
  - `production/`, `maintenance/` (Scenario 2)
  - `marketing/` (Scenario 3)
  - `actuals/`, `budget/`, etc. (Scenario 4)
  - `emissions/`, `energy/`, etc. (Scenario 5)

### 3. AI Transformations (Option C)

Si fichiers TXT existants :
1. Les convertir en CSV avec colonne `content`
2. Créer AI Skills pour extraction PII, sentiment, etc.
3. Appliquer sur colonne `content`

### 4. Créer Semantic Model

- Importer tables depuis Lakehouse
- Créer relations (voir `schema.md` de chaque scénario)
- Ajouter mesures DAX depuis `dax_measures.md`

### 5. Configurer Data Agent

- Créer Data Agent dans Fabric
- Utiliser `data_agent_instructions_clean.md` comme system prompt
- Tester avec questions de `data_agent_examples.md`

---

## 📊 Métriques de Validation

**Valeurs attendues par scénario** (dataset complet) :

| Scénario | Métrique Clé | Valeur Attendue |
|----------|--------------|-----------------|
| Call Center | CSAT | ~3.5-4.0/5 (70-80%) |
| Call Center | FCR | ~70% |
| Maintenance | OEE | ~75-80% |
| Maintenance | MTTR | ~100-120 min |
| Marketing | Campaign ROI | +100% à +500% |
| Marketing | Open Rate | ~22% |
| Finance | Gross Margin % | ~40-45% |
| Finance | DSO | ~30-45 days |
| ESG | Scope 3 % | ~70-80% du total |
| ESG | Renewable Energy % | ~25-35% (en progression) |
| HR | Attrition Rate | ~12-13% (benchmark < 15%) |
| HR | Promotion Rate | ~10% (benchmark 8-10%) |
| HR | Training Hours/FTE | ~42h (benchmark ≥ 40h) |
| HR | Internal Mobility Rate | ~14-15% (sain: 10-15%) |

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

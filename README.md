# Microsoft Fabric - Démos Customer 360 & ESG

**5 scénarios de démonstration** illustrant les capacités de Microsoft Fabric :
- OneLake + Shortcuts
- AI Shortcut Transformations (texte → données structurées)
- Fabric Data Agent (questions en langage naturel)
- Power BI Semantic Models (métriques métier)

---

## 📞 Scenario 1 - Call Center & Customer Service

**Cas d'usage** : Customer 360 avec analyse des appels clients

**Données** :
- **Commerce** : 1 000 clients, 800 produits, 15 000 commandes
- **Call Center** : 2 000 appels, 15 agents, transcripts texte (AI Transformations)

**Métriques clés** :
- CSAT (Customer Satisfaction Score)
- FCR (First Call Resolution)
- AHT (Average Handle Time)
- Repeat Call Rate

**Liens** :
- 📂 [Dossier Scenario 1](https://github.com/EtienneSIG/MF_CallCenter)


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
- 📂 [Dossier Scenario 2](https://github.com/EtienneSIG/MF_SupplyMaintenance)


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
- 📂 [Dossier Scenario 3](https://github.com/EtienneSIG/MF_MarketingCampaign)

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
- 📂 [Dossier Scenario 4](https://github.com/EtienneSIG/MF_Finance)


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


**Persona Data Agent** : ESG & Sustainability Manager

---

## 🛠️ Corrections Appliquées (Tous Scénarios)

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





# quanta-glottal-transcoder
# transcodeur quanta-glottique

Module de **transcodage QuantaGlottal©®** — conversion bidirectionnelle entre le format **QG** (QuantaGlottal) et des standards de représentation sémantique : **RDF**, **JSON-LD**, **OWL**, **Graph**.

---

## ✨ Fonctionnalités
- **Lecture/écriture QG** : chargement et sérialisation des glyphes QuantaGlottal©®
- **Export RDF/OWL** : conversion vers des graphes de connaissances interopérables
- **Import JSON-LD** : intégration de données sémantiques externes
- **Validation** : vérification de la conformité au schéma QG-Core
- **Mapping personnalisé** : adaptation des clés QG vers vocabulaires RDF/OWL spécifiques
- **Support Graph** : export/import de structures en graphe (NetworkX, GraphML, etc.)

---

## 📦 Installation (développement)
```bash
pip install -e .


---

⚡ Exemple rapide

from transcodeur_quanta_glottique import QGTranscoder

# Charger un fichier QG
t = QGTranscoder()
glyphs = t.load_qg("exemple.qg.json")

# Export en RDF/Turtle
t.to_rdf(glyphs, "sortie.ttl")

# Import depuis JSON-LD
data = t.from_jsonld("source.jsonld")
t.save_qg(data, "nouveau.qg.json")


---

🧱 Structure suggérée

src/transcodeur_quanta_glottique/
  __init__.py
  transcoder.py        # logique principale QG ↔ RDF/JSON-LD/OWL
  validators.py        # vérification schéma QG
  mappers/
    __init__.py
    rdf_mapper.py
    jsonld_mapper.py
    owl_mapper.py
tests/
  test_transcoder.py
pyproject.toml
.gitignore
LICENSE
README.md


---

🧪 Tests

pytest -q


---

🔐 Éthique

Le transcodage respecte l’intégrité et la sémantique des glyphes originaux.
Les conversions sont traçables et réversibles, garantissant la fidélité du sens.


---

📜 Licence

MIT — voir LICENSE.


---

Auteur : Frédéric Tabary — Institut IA
Contact : 0645605023 — Canada, Montréal, France
INSTITUT🦋 IA INC., 7100-380, rue Saint-Antoine Ouest, Montréal (Québec) H2Y 3X7.




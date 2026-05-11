# Protege-First-Project

This is my first project on [Protégé](https://protege.stanford.edu/)! 

It is a very simple OWL ontology built using **Protégé** for my Data Semantics course. 

## 🎯 Project Goals
The objective was to move from a theoretical model to a functional **TBox** that organizes and classifies **ABox** data. I used iterative reasoning to ensure that my axioms led to sound, automated inferences.

## 🏗️ Technical Specifications
This ontology satisfies specifications from Level 1 through Level 3, including:

### 1. Geographical Hierarchy
- Models **Continents, Countries, Regions, and Cities**.
- Uses **transitive properties** to handle geographical containment (e.g., if a city is in a region, and a region is in a country, the city is inferred to be in that country).
- Includes specific properties for **Capitals** and **Population** data.

### 2. Organizational Logic
- Models **Companies, NGOs, and Universities**.
- Implements the `hasHeadquartersIn` and `hasOfficesIn` properties.
- **Reasoning Task**: The ontology correctly infers the `NGO` type for underspecified individuals (like MSF) based on domain/range restrictions.

### 3. Advanced Axioms (Level 2 & 3)
- **Disjointness**: Ensures that an entity cannot be both a City and a Country simultaneously.
- **Functional Properties**: Applied to relationships where an entity can only have one value (like a specific headquarters).
- **Equivalent Classes**: Defined complex classes such as `EuropeanCountry` and `Capital` using Object Restrictions.

### 4. Personal Extension
I extended the original assignment by adding:
- **University** and **Student** branches.
- Modeled academic relationships (e.g., "Student attends University").
- Included myself as a `Student` instance to test the logic.

## 🛠️ How to View
1. Open [Protégé](https://protege.stanford.edu/).
2. Load the `.owl` file from the [root directory](./).
3. Start the **Hermit Reasoner** to see the inferred hierarchy and class memberships.

---

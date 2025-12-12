# Components

The CE-RISE DPP architecture is organized into three main groups of components, each containing functional layers with specific data models that maintain interoperability across the system.

## Architecture Components by Group

---

### A. Core Layers

Foundation components that are essential for every Digital Product Passport.

#### <u>Product Identification Layer</u>
I. **[Product Profile](product-profile.md)** - Defines the immutable identity, origin, and basic specification of the product (required)

#### <u>DPP Metadata Layer</u>
Models providing metadata for DPP record management and governance:

I. **[DPP Record Metadata](dpp-record-metadata.md)** - Semantic and structural metadata of the DPP record
  * Ontology bindings and schema references
  * Data model versions and profiles
  * Supported representation formats
  * Validation schemas
  
II. **[DPP Access and Governance](dpp-access-and-governance.md)** - Operational and access-related metadata
  * Access levels and permissions
  * Security settings
  * Data carrier specifications
  * Longevity policies
  * Interoperability configurations
  
III. **[DPP Record Custody](dpp-record-custody.md)** - Chain of custody and governance history
  * Custody event tracking
  * Custodian identification
  * Transfer authorizations
  * Integrity evidence (signatures, hashes)

---

### B. Value-Added Information Layers

Domain-specific components that provide rich information throughout the product lifecycle.

#### <u>Dynamic Lifecycle Layer</u>
Models capturing time-dependent changes and events:

I. **[Traceability and Lifecycle Events](traceability-and-life-cycle-events.md)** - Dynamic traceability and supply-chain events

II. **[Diagnostic Results](diagnostic-results.md)** - Structured outputs from diagnostic, repair, service, or condition-assessment operations

#### <u>Operation & Use Layer</u>
I. **[Usage and Maintenance](usage-and-maintenance.md)** - Product usage, service/repair actions, and instructions for operation and upkeep

#### <u>Impact Assessment Layer</u>
Models for comprehensive impact calculations:

I. **[Integrated LCA](integrated-lca.md)** - Environmental, social, and economic life cycle assessment data

II. **Product System** *(planned)* - Underlying data model for structuring activities, flows, and elementary exchanges

#### <u>Circularity & End-of-Life Layer</u>
Circularity metrics and end-of-life pathways:

I. **Circularity and EoL** *(planned)* - Design for circularity, performance scores, and end-of-life information

II. **[RE Indicators Specification](re-indicators-specification.md)** *(under development)* - Specific end-of-life indicators and recovery options

#### <u>Legal, Compliance & Standards Layer</u>
Regulatory and standards conformity:

I. **Compliance and Standards** *(planned)* - Regulatory compliance, certifications, and evidence documentation

II. **Conformity Requirements Specification** *(planned)* - Standard-specific data requirements and procedures

---

### C. Cross-Cutting Utility Layers

Reusable components that support data quality and reliability across all other layers.

#### <u>Uncertainty Layer</u>
I. **Uncertainty Quantification** *(planned)* - Generic structures for representing uncertainty in measurements, assessments, and indicators

#### <u>Data Quality Layer</u>
I. **Data Quality Framework** *(planned)* - Metadata for data quality, provenance, representativeness, completeness, and assessment pedigree

---


## Using the Components

### Modularity
Each component can be used independently or combined with others based on your specific use case requirements.

### Interoperability
All components follow standardized interfaces to ensure seamless integration across different systems and platforms.

### Extensibility
The architecture allows for custom extensions and additional models as new requirements emerge.

For detailed specifications and schemas for each model, visit the individual component pages or their respective repositories.

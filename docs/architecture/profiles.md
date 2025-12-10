# Profiles

Profiles are predefined compositions of data models from the CE-RISE DPP architecture that address specific use cases, industry requirements, or regulatory needs. They provide guidance on which models to combine for different scenarios while maintaining the flexibility of the modular architecture.

## Understanding Profiles

A profile is essentially a recipe that specifies:
- Which models from the architecture to include
- How these models relate to each other
- What level of detail is required for each model
- Optional extensions or customizations for specific contexts

## Profile Composition Strategy

### 1. Start with Core Layers (Always Required)

Every profile MUST include:
- **`product-profile`** - The foundational identity layer
- **`dpp-record-metadata`** - The semantic and structural metadata (when available)
- **`dpp-access-and-governance`** - Access and operational metadata (when available)
- **`dpp-record-custody`** - Chain of custody tracking (when available)

These provide the essential backbone for any Digital Product Passport implementation.

### 2. Add Value-Added Information Layers (As Needed)

Select from the five value-added layers based on your specific requirements:

#### For Supply Chain Transparency
Include from **Dynamic Lifecycle**:
- `traceability-and-lifecycle-events` - Track product journey
- `diagnostic-results` - Monitor condition over time

#### For Product Service & Support
Include from **Operation & Use**:
- `usage-and-maintenance` - Enable proper product care

#### For Sustainability Reporting
Include from **Impact Assessment**:
- `integrated-lca` - Environmental and social impacts
- `product-system` - Detailed system modeling

#### For Circular Economy
Include from **Circularity & End-of-Life**:
- `circularity-and-eol` - Design and performance metrics
- `re-indicators-specification` - Recovery pathways

#### For Regulatory Compliance
Include from **Legal, Compliance & Standards**:
- `compliance-and-standards` - Meet legal requirements
- `conformity-requirements-specification` - Industry standards

### 3. Apply Cross-Cutting Utility Layers (For Quality)

Enhance data reliability by including:
- **`uncertainty-quantification`** - When dealing with estimates or predictions
- **`data-quality-framework`** - When data provenance and trust are critical

## Example Profiles

### Basic Product Tracking Profile
*Minimal DPP for simple supply chain visibility*

**Core Layers:**
- `product-profile` ✓
- `dpp-record-metadata` ✓
- `dpp-access-and-governance` ✓
- `dpp-record-custody` ✓

**Value-Added Layers:**
- `traceability-and-lifecycle-events` (basic events only)

**Cross-Cutting Layers:**
- None required

### Full Circular Economy Profile
*Comprehensive DPP for circular business models*

**Core Layers:**
- `product-profile` ✓
- `dpp-record-metadata` ✓
- `dpp-access-and-governance` ✓
- `dpp-record-custody` ✓

**Value-Added Layers:**
- `traceability-and-lifecycle-events` ✓
- `diagnostic-results` ✓
- `usage-and-maintenance` ✓
- `integrated-lca` ✓
- `product-system` ✓
- `circularity-and-eol` ✓
- `re-indicators-specification` ✓

**Cross-Cutting Layers:**
- `uncertainty-quantification` ✓
- `data-quality-framework` ✓

### Regulatory Compliance Profile (ESPR)
*Meeting EU Ecodesign for Sustainable Products Regulation requirements*

**Core Layers:**
- `product-profile` ✓
- `dpp-record-metadata` ✓
- `dpp-access-and-governance` ✓
- `dpp-record-custody` ✓

**Value-Added Layers:**
- `traceability-and-lifecycle-events` (selected fields)
- `usage-and-maintenance` (repair information)
- `integrated-lca` (environmental only)
- `circularity-and-eol` (recycled content, recyclability)
- `compliance-and-standards` ✓
- `conformity-requirements-specification` ✓

**Cross-Cutting Layers:**
- `data-quality-framework` (for compliance documentation)

### Service & Maintenance Profile
*For products requiring active service management*

**Core Layers:**
- `product-profile` ✓
- `dpp-record-metadata` ✓
- `dpp-access-and-governance` ✓
- `dpp-record-custody` ✓

**Value-Added Layers:**
- `diagnostic-results` ✓
- `usage-and-maintenance` ✓
- `traceability-and-lifecycle-events` (service events)

**Cross-Cutting Layers:**
- `uncertainty-quantification` (for predictive maintenance)

## Creating Custom Profiles

### Step 1: Define Your Objectives
- What is the primary purpose of your DPP?
- Who are the stakeholders that will use it?
- What decisions will be made based on the data?

### Step 2: Map Requirements to Layers
- List all data requirements
- Match each requirement to the appropriate layer and model
- Identify dependencies between models

### Step 3: Determine Data Quality Needs
- Assess where uncertainty quantification is valuable
- Identify where data provenance is critical
- Decide on quality metadata requirements

### Step 4: Document Your Profile
- Create a clear specification listing all included models
- Define required vs. optional fields within each model
- Specify any custom extensions or constraints
- Document integration points between models

## Profile Validation

When implementing a profile, ensure:

1. **Completeness**: All Core Layers are present
2. **Coherence**: Selected models work together logically
3. **Feasibility**: Data can realistically be collected and maintained
4. **Compliance**: Regulatory requirements are met
5. **Interoperability**: Standard interfaces are maintained

## Industry-Specific Profiles

Different industries may develop standardized profiles:

### Electronics & Batteries
- Focus on material composition, repair information, and recycling
- Heavy emphasis on compliance and hazardous substances

### Textiles & Fashion
- Emphasis on supply chain transparency and social impacts
- Strong circularity and end-of-life components

### Construction Materials
- Product-system modeling for complex assemblies
- Long-term performance and maintenance data

### Automotive
- Complete lifecycle tracking with diagnostic integration
- Comprehensive impact assessment and circularity metrics

## Profile Evolution

Profiles are not static and can evolve:

1. **Start Simple**: Begin with core requirements
2. **Add Incrementally**: Expand as needs grow
3. **Maintain Compatibility**: Ensure backward compatibility
4. **Version Control**: Track profile versions explicitly

## Best Practices

### Do's
- ✓ Start with established profiles when possible
- ✓ Document your profile decisions clearly
- ✓ Consider future extensibility
- ✓ Validate against real-world data availability
- ✓ Test interoperability with partner systems

### Don'ts
- ✗ Include models without clear purpose
- ✗ Over-specify requirements initially
- ✗ Ignore cross-cutting quality layers
- ✗ Create incompatible variations
- ✗ Forget about maintenance burden

## Getting Started

1. Review the [Architecture Overview](index.md) to understand available models
2. Study relevant example profiles above
3. Consult the [Implementation Plan](../roadmap/implementation.md) for model availability
4. Begin with a minimal viable profile
5. Iterate based on stakeholder feedback

Remember: The modular architecture allows you to start simple and expand over time. Not every DPP needs every model - choose what adds value for your specific use case.
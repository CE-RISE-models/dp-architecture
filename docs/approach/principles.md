# Approach

Instead of being top-down, we use a bottom-up approach of separate independent modules, supported by cross-cutting models that can be reused in different places and with the possibility of having overlapped models where different models are used to represent the same information.

## Core Foundation: Product-Profile

This is achieved by prescribing only one core model component: the **product-profile**. This is the way by which the passport can be associated with the product and contains immutable data about the product.

In the analogy with the human passport, this is like the name and date of birth - immutable information to identify the user, or even the fingerprints in the RFID chip of the passport (maybe also the picture, though people and pictures need to be updated some time).

## Modular Composition

All the rest is optional and composable. This bottom-up approach enables:

- **Independent modules** that can be developed and maintained separately
- **Cross-cutting models** that provide reusable components across different contexts
- **Overlapped models** allowing different representations of the same information
- **Flexible composition** based on specific needs and requirements

## User-Driven Profiles

Users are provided the possibility to build profiles of DPP data models to create tailored data structures for:

- Representing information in contexts specific to their needs
- Storing data according to their technical and business requirements  
- Making sense of information stored in DPPs across different systems and standards

## Flexibility Benefits

This flexibility in the approach allows sophisticated data representations to be easy and less expensive to deploy, but also to be adopted. We do not want to force users into filling in everything but to give the opportunity to use rich information. Hence the possibility to represent traceability, uncertainty, assess data quality, compliance, etc. - all possible and integratable, at low cost for both system designers and system users.

This approach ensures that while maintaining a common foundation through the product-profile, the architecture remains flexible and adaptable to diverse use cases and evolving requirements.
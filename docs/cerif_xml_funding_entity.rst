.. _funding:


Funding
=======
:Examples: `openaire_cerif_xml_example_fundings.xml <https://github.com/openaire/guidelines-cris-managers/blob/master/samples/openaire_cerif_xml_example_fundings.xml>`_
:Representation: XML element ``Funding``; the rest of this section documents children of this element
:CERIF: the Funding entity (`<https://w3id.org/cerif/model#Funding>`_)


Internal Identifier
^^^^^^^^^^^^^^^^^^^
:Use: mandatory (1)
:Representation: XML attribute ``id``
:CERIF: the FundingIdentifier attribute (`<https://w3id.org/cerif/model#Funding.FundingIdentifier>`_)


Type
^^^^
:Description: The type of the funding
:Use: mandatory (1)
:Representation: XML element ``Type`` from namespace ``https://www.openaire.eu/cerif-profile/vocab/OpenAIRE_Funding_Types``
:CERIF: the Funding_Classification (`<https://w3id.org/cerif/model#Funding_Classification>`_)
:Vocabulary: Types of funding for the OpenAIRE Guidelines for CRIS Managers

  * **Funding Programme** (`<https://www.openaire.eu/cerif-profile/vocab/OpenAIRE_Funding_Types#FundingProgramme>`_): A funding programme or a similar scheme that funds some number of proposals. Funding programmes can be broken down into sub-programmes.
  * **Call** (`<https://www.openaire.eu/cerif-profile/vocab/OpenAIRE_Funding_Types#Call>`_): Call for proposals: a specific campaign for the funder to solicit proposals from interested researchers and institutions.
  * **Tender** (`<https://www.openaire.eu/cerif-profile/vocab/OpenAIRE_Funding_Types#Tender>`_): Tender for services or deliveries: a specific campaign for the funder to solicit offers for services or deliveries.
  * **Gift** (`<https://www.openaire.eu/cerif-profile/vocab/OpenAIRE_Funding_Types#Gift>`_): A donation connected with specific terms and conditions.
  * **Internal Funding** (`<https://www.openaire.eu/cerif-profile/vocab/OpenAIRE_Funding_Types#InternalFunding>`_): Internal funds used to amend or replace external funding.
  * **Contract** (`<https://www.openaire.eu/cerif-profile/vocab/OpenAIRE_Funding_Types#Contract>`_): 
  * **Award** (`<https://www.openaire.eu/cerif-profile/vocab/OpenAIRE_Funding_Types#Award>`_): 
  * **Grant** (`<https://www.openaire.eu/cerif-profile/vocab/OpenAIRE_Funding_Types#Grant>`_): 



Acronym
^^^^^^^
:Description: The acronym of the funding
:Use: optional (0..1)
:Representation: XML element ``Acronym``
:CERIF: the Funding.Acronym attribute (`<https://w3id.org/cerif/model#Funding.Acronym>`_)



Name
^^^^
:Description: The name of the funding
:Use: optional, possibly multiple (0..*)
:Representation: XML element ``Name`` as a multilingual string
:CERIF: the Funding.Name attribute (`<https://w3id.org/cerif/model#Funding.Name>`_)



Amount
^^^^^^
:Description: The amount of the funding and its currency
:Use: optional (0..1)
:Representation: XML element ``Amount``
:CERIF: the Funding.Amount https://w3id.org/cerif/model#Funding.CurrencyCode attribute (`<https://w3id.org/cerif/model#Funding.Amount https://w3id.org/cerif/model#Funding.CurrencyCode>`_)



Description
^^^^^^^^^^^
:Description: A description of the funding
:Use: optional, possibly multiple (0..*)
:Representation: XML element ``Description`` as a multilingual string
:CERIF: the Funding.Description attribute (`<https://w3id.org/cerif/model#Funding.Description>`_)



Keyword
^^^^^^^
:Description: A single keyword or key expression. Please repeat to serialize separate keywords or key expressions.
:Use: optional, possibly multiple (0..*)
:Representation: XML element ``Keyword`` as a multilingual string
:CERIF: the Funding.Keywords attribute (`<https://w3id.org/cerif/model#Funding.Keywords>`_)



Funder
^^^^^^
:Description: The funder or funders
:Use: optional, possibly multiple (0..*)
:Representation: XML element ``Funder`` with embedded XML element ``OrgUnit`` or ``Person``
:CERIF: the OrganisationUnit_Funding linking entity (`<https://w3id.org/cerif/model#OrganisationUnit_Funding>`_) with the `<https://w3id.org/cerif/vocab/OrganisationFundingEngagements#Funder>`_ semantics


PartOf
^^^^^^
:Description: Chain up to the larger funding that encompasses this funding
:Use: optional (0..1)
:Representation: XML element ``PartOf`` with embedded XML element ``Funding``
:CERIF: the Funding_Funding linking entity (`<https://w3id.org/cerif/model#Funding_Funding>`_) with the `<https://w3id.org/cerif/vocab/Inter-­FundingRelations#Part>`_ semantics (direction :1)


Supports
^^^^^^^^
:Description: A project supported by this funding
:Use: optional, possibly multiple (0..*)
:Representation: XML element ``Supports`` with embedded XML element ``Project``
:CERIF: the Project_Funding linking entity (`<https://w3id.org/cerif/model#Project_Funding>`_) with the `<https://w3id.org/cerif/vocab/ProjectFundingRelations#Support>`_ semantics


Duration
^^^^^^^^
:Description: Duration of the funding
:Use: optional (0..1)
:Representation: XML element ``Duration`` *TODO*
:CERIF: the Funding_Classification linking entity (`<https://w3id.org/cerif/model#Funding_Classification>`_) with the `<https://w3id.org/cerif/vocab/Durations#FundingDuration>`_ semantics




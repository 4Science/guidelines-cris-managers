.. _patent:


Patent
======
:Description: A set of exclusive rights granted by a sovereign state to an inventor or assignee for a limited period of time in exchange for detailed public disclosure of an invention. Source: Wikipedia
:Representation: XML element ``Patent``; the rest of this section documents children of this element
:CERIF: the ResultPatent entity (`<https://w3id.org/cerif/model#ResultPatent>`_)


Internal Identifier
^^^^^^^^^^^^^^^^^^^
:Use: mandatory (1)
:Representation: XML attribute ``id``
:CERIF: the ResultPatentIdentifier attribute (`<https://w3id.org/cerif/model#ResultPatent.ResultPatentIdentifier>`_)


Type
^^^^
:Description: The type of the patent (currently just one option)
:Use: mandatory (1)
:Representation: XML element ``Type`` from namespace ``https://www.openaire.eu/cerif-profile/vocab/COAR_Patent_Types``
:CERIF: the ResultPatent_Classification (`<https://w3id.org/cerif/model#ResultPatent_Classification>`_)
:Vocabulary: Patent types extracted from the COAR Resource Types concept scheme: Types of patents as extracted from the COAR Resource Types concept scheme (http://vocabularies.coar-repositories.org/documentation/resource_types/, the term 'patent' only).

  * **patent** (`<http://purl.org/coar/resource_type/c_15cd>`_): A patent or patent application.



Title
^^^^^
:Use: optional, possibly multiple (0..*)
:Representation: XML element ``Title`` as a multilingual string
:CERIF: the ResultPatent.Title attribute (`<https://w3id.org/cerif/model#ResultPatent.Title>`_)



VersionInfo
^^^^^^^^^^^
:Use: optional, possibly multiple (0..*)
:Representation: XML element ``VersionInfo`` as a multilingual string
:CERIF: the ResultPatent.VersionInfo attribute (`<https://w3id.org/cerif/model#ResultPatent.VersionInfo>`_)



RegistrationDate
^^^^^^^^^^^^^^^^
:Use: optional (0..1)
:Representation: XML element ``RegistrationDate``
:CERIF: the ResultPatent.RegistrationDate attribute (`<https://w3id.org/cerif/model#ResultPatent.RegistrationDate>`_)



ApprovalDate
^^^^^^^^^^^^
:Use: optional (0..1)
:Representation: XML element ``ApprovalDate``
:CERIF: the ResultPatent.ApprovalDate attribute (`<https://w3id.org/cerif/model#ResultPatent.ApprovalDate>`_)



CountryCode
^^^^^^^^^^^
:Use: optional (0..1)
:Representation: XML element ``CountryCode``
:CERIF: the ResultPatent.CountryCode attribute (`<https://w3id.org/cerif/model#ResultPatent.CountryCode>`_)



PatentNumber
^^^^^^^^^^^^
:Use: optional (0..1)
:Representation: XML element ``PatentNumber``
:CERIF: the ResultPatent.PatentNumber attribute (`<https://w3id.org/cerif/model#ResultPatent.PatentNumber>`_)



Identifier
^^^^^^^^^^
:Description: An identifier of this patent
:Use: optional, possibly multiple (0..*)
:Representation: XML element ``Identifier`` with mandatory ``type`` attribute
:CERIF: the FederatedIdentifier entity (``https://w3id.org/cerif/model#FederatedIdentifier``)



Abstract
^^^^^^^^
:Use: optional, possibly multiple (0..*)
:Representation: XML element ``Abstract`` as a multilingual string
:CERIF: the ResultPatent.Abstract attribute (`<https://w3id.org/cerif/model#ResultPatent.Abstract>`_)



Subject
^^^^^^^
:Description: The subject of the patent from a classification
:Use: optional, possibly multiple (0..*)
:Representation: XML element ``Subject`` containing the classification identifier and having a ``scheme`` attribute to specify the classification scheme identifier
:CERIF: the ResultPatent_Classification (`<https://w3id.org/cerif/model#ResultPatent_Classification>`_)


Keyword
^^^^^^^
:Description: A single keyword or key expression. Please repeat to serialize separate keywords or key expressions.
:Use: optional, possibly multiple (0..*)
:Representation: XML element ``Keyword`` as a multilingual string
:CERIF: the ResultPatent.Keywords attribute (`<https://w3id.org/cerif/model#ResultPatent.Keywords>`_)



OriginatesFrom
^^^^^^^^^^^^^^
:Use: optional, possibly multiple (0..*)
:Representation: XML element ``OriginatesFrom`` with embedded XML element ``Project`` or ``Funding``
:CERIF: the Project_ResultPatent linking entity (`<https://w3id.org/cerif/model#Project_ResultPatent>`_) with the `<https://w3id.org/cerif/vocab/Project_Output_Roles#Originator>`_ semantics; the ResultPatent_Funding linking entity (`<https://w3id.org/cerif/model#ResultPatent_Funding>`_) with the `<https://w3id.org/cerif/vocab/Funding_Output_Roles#Originator>`_ semantics


References
^^^^^^^^^^
:Description: Result outputs that are referenced by this patent
:Use: optional, possibly multiple (0..*)
:Representation: XML element ``References`` with embedded XML element ``Publication`` or ``Patent`` or ``Product``
:CERIF: the ResultPatent_ResultPublication linking entity (`<https://w3id.org/cerif/model#ResultPatent_ResultPublication>`_) with the `<https://w3id.org/cerif/vocab/Inter-OutputRelations#Reference>`_ semantics (direction :1); the ResultPatent_ResultProduct linking entity (`<https://w3id.org/cerif/model#ResultPatent_ResultProduct>`_) with the `<https://w3id.org/cerif/vocab/Inter-OutputRelations#Reference>`_ semantics (direction :1); the ResultPatent_ResultPatent linking entity (`<https://w3id.org/cerif/model#ResultPatent_ResultPatent>`_) with the `<https://w3id.org/cerif/vocab/Inter-OutputRelations#Reference>`_ semantics (direction :1)




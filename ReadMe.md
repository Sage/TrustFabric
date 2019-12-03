Trust Fabric
============

Definition
----------

The Trust Fabric is a technology to facilitate trust within a business community. The service maps relationships with inferred trust to a cryptographically secure network of trust that allows businesses to connect, transact, process and automate securely. By leveraging existing network insights, the Trust Fabric acts as a trust facilitator rather than a trust authority, and makes trust programmable.

The Trust Fabric is a foundation service. It enables electronic transaction exchange between parties in a secure, auditable, and open manner, whilst maintaining confidentiality between parties at all times. Examples of such transactions include tax submissions, purchase orders, sales invoices, payment instructions and payslips. The service is only concerned with trust facilitation and auditability; it is not concerned with the transport of messages. 

Inherently there are many networks of trust, and to allow for such plurality the service is designed for interoperability and to an open specification.

Public Launch
-------------

The Trust Fabric concept was initially made public on December 3rd 2019 at the AWS Re:Invent conference in Las Vegas by Sage in conjunction with AWS, a key technology partner. Links to the video recording can be found here (tbc) and the slides here (tbc).

Request for Collaboration
-------------------------

Whilst Sage is kick-starting the Trust Fabric initiative, the aim is to work in a collaborative and open way with other organisations who could benefit from the trust established by such a technology - particularly as this is an industry-wide problem which requires an open, industry-wide solution. With this in mind, the code developed by Sage in support of the Trust Fabric will be published here in this Github repository under open-source. We welcome collaboration opportunities or re-use of our work within other organisations.

Fundamental Purpose
-------------------

The Trust Fabric proves for any transaction expressed as a JSON document:

  * Provenance of the document, i.e. who within the Trust Fabric created the document.
  * Actuality of the document, i.e. at what point in time it existed.
  * Integrity of the document, i.e. that its content wasn’t tampered by any rogue actor. 
  * Assertions recorded against the document, i.e. key events that happened to a document subsequently.
  
  The Trust Fabric can provide these assurance without recording the actual content of a document or its recipient,as parties may not wish to disclose such information for confidentiality or data privacy reasons. Optionally the Trust Fabric can harness network insights to appraise the 'trustworthiness' of network parties. 

What the Trust Fabric Enables
-----------------------------

Being able to determine provenance, actuality, integrity and assertions programmatically opens a wide range of use cases: 

  * Reduce invoice fraud by verifying the integrity of the invoice and performing a background check on the issuer.
  * Reduce invoice fraud by cascading bank detail changes safely.  
  * Automate the Accounts Payable (AP) process by allowing programmatic document verification.
  * Eliminate manual steps in a financial audit.
  * Provide a self-service to instantly verify payslips.
  * Provide proof when a tax return was filed and verify its content.
  * Secure payment out instructions and track its subsequent progress.
  * Allow direct document exchange and eliminate email through secure pairing
  * Allow a business loan to be registered against an invoice

Amazon Quantum Ledger Database (QLDB) 
-------------------------------------

The default implementation of Trust Fabric is based on Amazon QLDB to ensure the integrity and auditability of the trust ledger i.e. the data recorded by Trust Fabric. This make the trust ledger immutable and cryptographically verifiable. 

Trust Fabric adds programmable trust to an existing network and is therefore well aligned to QLDB’s model of a centralised, trusted entity. Whilst classic blockchain frameworks such as Hyperledger and Ethereum can be deployed to similar effect, Trust Fabric does not require decentralised ledger and consensus capabilities, and can therefore take advantage of the performance and operational efficency offered by QLDB. 

What to Expect Next
-------------------

For now this Github repository is a holding pattern. We will share progress here as the Trust Fabric initiatives takes shape. In due course we intend to publish:

* Algorithms and sample implementation to calculate the digest/hash of a document
* API specification for all public endpoints for document verification, document assertions, and Trust Fabric federation.
* Naming conventions and taxonomies.
* Supporting code and sample implementations.   

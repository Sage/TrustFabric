Trust Fabric
============

Definition
----------

The Trust Fabric is a technology to facilitate trust within a business community. The service maps relationships with implied trust to a cryptographically secure network of trust that allows businesses to connect, transact, process and automate with confidence. Inherently there are many networks of trust, so to allow for such plurality the Trust Fabric service is designed for interoperability, and to an open specification.

Public Launch
-------------

The Trust Fabric concept was initially made public on December 3rd 2019 at the AWS Re:Invent conference in Las Vegas, by Klaus-Michael Vogelberg, Chief Architect of Sage PLC, in conjunction with AWS, key technology partner.  Links to the video recording can be found here (tbc) and the slides here (tbc).

Request for Collaboration
-------------------------

Whilst Sage is kick-starting the Trust Fabric initiative, the aim is to work in a collaborative and open way with other organisations who could benefit from the trust established by such a technology - particularly as this is an industry-wide problem which requires an open, industry-wide solution.  With this in mind, all of the code developed within Sage in support of the Trust Fabric will be published here in this Github repository as open-source software.  We welcome collaboration opportunities or re-use of our work within other organisations.

Overview
--------
Trust Fabric is a foundation service that facilitates electronic transactions between parties in a secure, auditable, and open manner. Examples of such transactions include tax submissions, purchase orders, sales invoices, payment instructions and payslips. 

Fundamental Purpose
-------------------

For any given document, the Trust Fabric proves: 
  * Provenance of the document, i.e. who within the Trust Fabric created the document.
  * Existence of the document, i.e. that it existed at the point in time it was recorded in the trust ledger of the service.
  * Integrity of the document, i.e. that its content wasn’t tampered by any rogue actor. 
  * Assertions recorded against the document by the creator or any other members of the Trust Fabric.
  * Assertions recorded against the identity by authorised subsystems of the Trust Fabric.

Crucially the service can provide such proof without knowing the content of a document:
  * The content may be business confidential which the parties may not wish to disclose to the Trust Fabric operator.
  * The Trust Fabric operator may not be willing to take on the operational risks of storing confidential content. 

What the Trust Fabric Enables
-----------------------------

Whilst the concepts behind the Trust Fabric might appear somewhat abstract, the scenarios it enables are very tangible. Here are a few illustrative use cases how the trust network service can be used:
  * Reduce invoice fraud by verifying the integrity of the invoice and performing a background check on the issuer.
  * Reduce invoice fraud by cascading bank detail changes safely.  
  * Automate Accounts Payable (AP) process by allowing programmatic document verification.
  * Automate the AP audit process.
  * Provide a self-service to verify pay slips.
  * Provide proof when a tax return was filed and verify its content.
  * Secure payment out instructions and track its subsequent progress.
  * Allow direct document exchange and eliminate email through secure pairing
  * Allow a business loan to be registered against an invoice

Definitions
-----------

  * One or several SaaS applications and services make up a Trust Fabric.
  * The actors within the fabric are called identities. An identity denotes either a SaaS tenant, or an internal domain service provider such as HMRC or connected banks. An identity is represented by a GUID.
  * Documents are in its most basic form JSON objects, represented by a hash that gets calculated over a canonicalized representation. The algorithm will be in the public domain. 
  * Each document has a creator identity.
  * Each document consists of an envelope with standardised properties, and a payload with application-defined content.

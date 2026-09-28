=======
Roadmap
=======

Where **Quality Management System** is today, and what comes next. The plan follows the clauses of ISO 9001 an
external auditor asks about, so each step closes a gap you would otherwise cover with a spreadsheet. We do not
publish dates we cannot keep: items are listed in the order we build them.

.. seealso::
   :doc:`faq` — answers to the questions and messages people meet most often.

Available now (Odoo 20.0)
=========================

.. list-table::
   :header-rows: 1
   :widths: 30 20 50

   * - App
     - Price
     - What it covers
   * - **Quality Management System** (free core)
     - Free, LGPL-3
     - The nonconformity register (ISO 9001 §10.2) with the disposition of nonconforming output, concessions, holds and
       customer notification (§8.7), the clause libraries with the clauses declared not applicable (§4.3), the quality
       dashboard, the tamper-evident trail and electronic signatures. See :doc:`nonconformities` and :doc:`clauses`.
   * - Free bridges: Stock, Manufacturing, Purchase, Repair, Product
     - Free
     - Raise a nonconformity from the record where the problem was found. See :doc:`sources`.
   * - **QMS Advanced**
     - One-time purchase
     - Corrective actions with an independent effectiveness verdict (§10.2), internal audits with a risk-based
       programme (§9.2), document control with the quality policy, external documents and record retention (§5.2,
       §7.5), management review fed by every register (§9.3) and the one-click audit pack. See
       :doc:`corrective_actions`, :doc:`audits`, :doc:`documents`, :doc:`management_reviews` and :doc:`audit_pack`.
   * - **Context and scope**
     - Included in QMS Advanced
     - Internal and external issues, interested parties and their needs, and the signed scope (§4.1–4.3). See
       :doc:`context`.
   * - **Risks and opportunities**
     - Included in QMS Advanced
     - A 5 × 5 register with treatment decisions, treatment actions and re-assessment (§6.1). See :doc:`risks`.
   * - **Quality objectives**
     - Included in QMS Advanced
     - Objectives with their plan, measurements, status, policy link and communication (§6.2). See :doc:`objectives`.
   * - **Customer satisfaction**
     - Included in QMS Advanced
     - Satisfaction results made comparable, the complaint trend and improvement actions (§9.1.2). See
       :doc:`satisfaction`.
   * - **Equipment calibration**
     - Included in QMS Advanced
     - The equipment register, calibrations with traceability, adjustment protection and the out-of-tolerance impact
       assessment (§7.1.5). See :doc:`calibration`.
   * - **Training and competence**
     - Free with QMS Advanced, a separate module
     - The competence matrix, competence records, trainings with an effectiveness check and the internal auditor
       qualification (§7.2). The read-and-understood acknowledgements of controlled documents stay evidence of awareness
       (§7.3): they are not competence records. A separate free module, installed separately. See :doc:`competence`.
   * - **Supplier evaluation**
     - Free with QMS Advanced, a separate module
     - Supplier rating from receipts and supplier nonconformities or by periodic assessment, the approved supplier list
       by signed decisions, the purchase confirmation control, SCARs and the requirements communicated (§8.4). A
       separate free module, installed separately; its receipt measures install themselves with Inventory. See
       :doc:`suppliers`.
   * - Portal document readers
     - Free with QMS Advanced, a separate module
     - People without an internal user read and acknowledge controlled documents in My Account. A separate free module
       that installs itself with Portal. See :ref:`documents-portal-readers`.

Every app is a one-time purchase for its Odoo version: no subscription, no licence key, nothing that expires.

Other ISO standards
===================

**ISO 9001** is the standard the apps are built for. For **ISO 14001, ISO 45001, ISO 22000 and ISO 13485**, the apps
ship the *clause libraries* today: you can tag nonconformities and other records with their clauses and see the
evidence per clause (see :doc:`clauses`). The registers each of those standards asks for are not built yet. They
are planned as part of **QMS Advanced**, included in its price, one standard at a time:

.. list-table::
   :header-rows: 1
   :widths: 25 75

   * - Standard
     - What QMS Advanced will add
   * - **ISO 14001** (environment)
     - Environmental aspects and impacts, compliance obligations (legal register), emergency preparedness.
   * - **ISO 45001** (health and safety)
     - Hazard identification and risk assessment, incidents and near misses, consultation and participation of
       workers.
   * - **ISO 22000** (food safety)
     - HACCP plan, critical control points and their monitoring, prerequisite programmes.
   * - **ISO 13485** (medical devices)
     - Design and development controls, complaint handling and vigilance reporting, software validation.

Until then, keep those registers where you keep them today and use the clause libraries to link your
records to the standard.

Later
=====

- **Optional bridges to other Odoo apps**: calibration with the Maintenance app, the competence records mirrored in
  the employee skills, and satisfaction scores imported from Survey.
- **A supplier portal**: suppliers answer their corrective action requests and acknowledge requirements online.
- **A read-only portal for external auditors**: the clause view and the audit pack, without an Odoo licence seat.
- **Industry packs**, priced separately: automotive and aerospace (IATF 16949, AS9100), and laboratories
  (ISO/IEC 17025: calibration uncertainty and laboratory depth).
- **Explanations with AI**: for a nonconformity, the chain of evidence and ranked root-cause candidates, each
  citing the records used; and "was this done per procedure?" for any record. It will run on your own Anthropic
  key, so you pay the provider directly and see every cost.

What we will not build
======================

Some things stay out on purpose, so the apps stay focused:

- a survey tool (use the one you have and record its result as a customer satisfaction record);
- a helpdesk for complaints (complaints enter as nonconformities of source *Complaint*);
- laboratory calibration mathematics outside the ISO/IEC 17025 pack.

New Odoo versions
=================

Each app is ported to the next major Odoo version. A new version is a separate build on the Odoo Apps store, as
for every app there.

Your say
========

The order above comes from what auditors ask for and what users tell us. If something you need is missing, or
should come sooner, tell us through the app's page on the Odoo Apps store.

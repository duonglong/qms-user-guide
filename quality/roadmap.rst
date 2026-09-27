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
     - The nonconformity register (ISO 9001 §10.2), clause libraries for ISO 9001, 14001, 45001, 13485 and 22000,
       the quality dashboard, the tamper-evident trail and electronic signatures. See :doc:`nonconformities`.
   * - Free bridges: Stock, Manufacturing, Purchase, Repair, Product
     - Free
     - Raise a nonconformity from the record where the problem was found. See :doc:`sources`.
   * - **Core QMS**
     - One-time purchase
     - Corrective actions with an independent effectiveness verdict (§10.2), internal audits (§9.2), document control
       (§7.5), management review (§9.3) and the one-click audit pack. See :doc:`corrective_actions`, :doc:`audits`,
       :doc:`documents`, :doc:`management_reviews` and :doc:`audit_pack`.

Every app is a one-time purchase for its Odoo version: no subscription, no licence key, nothing that expires.

Next: Core QMS 1.1
==================

**Quality objectives** (ISO 9001 §6.2 and §9.1.3). Set objectives with a target and a period, record the actual
figure, and see them as an input of the management review, which needs them to be complete. Included in Core QMS.

Release 2
=========

The rest of the ISO 9001 clauses an auditor opens with, each where it fits best:

.. list-table::
   :header-rows: 1
   :widths: 25 12 63

   * - Area
     - Clause
     - What it will do
   * - **Risks and opportunities**
     - §6.1
     - A register with likelihood and severity, treatment actions (the same corrective actions you already use),
       and links to processes and nonconformities. Included in Core QMS.
   * - **Supplier evaluation**
     - §8.4
     - A rating per supplier computed from receipts and supplier nonconformities, an approved supplier list, and a
       corrective action request sent to the supplier. With the Purchase bridge.
   * - **Training and competence**
     - §7.2
     - A competence matrix by role, training records with expiry dates, and the read-and-understood
       acknowledgements of controlled documents you already have. A separate add-on.
   * - **Equipment calibration**
     - §7.1.5
     - An equipment register with calibration intervals and due dates; an out-of-tolerance result raises a
       nonconformity.
   * - **Customer satisfaction**
     - §9.1.2
     - A satisfaction input for the management review: a survey score or the trend of complaints for the period.

Later
=====

- **Industry packs**, priced separately: food safety (HACCP), medical devices (ISO 13485), automotive and aerospace
  (IATF 16949, AS9100), and laboratories (ISO/IEC 17025: calibration uncertainty and laboratory depth).
- **A read-only portal for external auditors**: the clause view and the audit pack, without an Odoo licence seat.
- **Explanations with AI**: for a nonconformity, the chain of evidence and ranked root-cause candidates, each
  citing the records used; and "was this done per procedure?" for any record. It will run on your own Anthropic
  key, so you pay the provider directly and see every cost.

What we will not build
======================

Some things stay out on purpose, so the apps stay focused:

- a survey tool (use the one you have and bring its score to the management review);
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

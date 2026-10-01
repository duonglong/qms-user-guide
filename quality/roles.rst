================
Roles and access
================

The **Quality** app has three roles. Each one gives access to the app and decides what a person can see and do in
it. Some decisions also depend on the person's place on the record — its owner, its author, its verifier, the lead
auditor, the chair — and a few are kept apart on purpose, so that nobody approves their own work.

The three roles
===============

.. list-table::
   :header-rows: 1
   :widths: 20 30 50

   * - Role
     - Includes
     - Meant for
   * - :guilabel:`User`
     - Internal user access to Odoo.
     - People who raise and treat nonconformities, carry out corrective actions, write document versions and read
       the documents addressed to them. Shop-floor staff who report problems get this role.
   * - :guilabel:`Internal auditor`
     - Everything a :guilabel:`User` has.
     - People who must read the whole quality system: they read every nonconformity, action, audit, document and
       management review of their companies, run the internal audits they are assigned to and request audit packs.
   * - :guilabel:`Manager`
     - Everything an :guilabel:`Internal auditor` has.
     - The people who run the quality system: they close, cancel and amend, approve documents, close audits, manage
       the configuration and change the settings.

The roles build on each other: a manager can do everything an internal auditor can, and an internal auditor
everything a user can. A person without any Quality role does not see the **Quality** app.

At installation, the administrator is a quality manager.

Three kinds of people take part without a Quality role:

- **Top management**, named in the Quality settings, approve the quality policy from their to-do. See
  :ref:`documents-top-management`.
- **Portal readers**, without an internal user, read and acknowledge the controlled documents that name them in their
  My Account portal, and see nothing else. See :ref:`documents-portal-readers`.
- **Employees** without a user are covered by the Training & Competence add-on: their competence records and trainings
  are kept on their employee record. See :doc:`competence`.
- **Every employee** — any internal user, with or without a Quality role — reports incidents and hazards from the
  **Safety reports** app once the environment, health and safety registers are switched on, and follows their own
  reports there. See :doc:`safety_reports`.

Give a user a role
==================

#. Go to :menuselection:`Settings --> Users & Companies --> Users` and open the user.
#. On the :guilabel:`Access Rights` tab, find the :guilabel:`Supply Chain` section.
#. In the :guilabel:`Quality` field, choose :guilabel:`User`, :guilabel:`Internal auditor` or :guilabel:`Manager`.
   Leave it empty to remove access to the app.
#. Save.

Only one Quality role can be chosen: each role already includes the ones before it.

.. tip::
   Give the Quality :guilabel:`User` role to everyone who must read and acknowledge controlled documents. Audience
   members without it are not asked to read: the version's chatter names them instead. See :doc:`documents`.

What each role sees
===================

Each role sees a different part of the records. Everything outside that part is hidden: it does not appear in lists,
on the dashboard, in the clause view or in exports.

.. list-table::
   :header-rows: 1
   :widths: 22 30 24 24

   * - Records
     - User
     - Internal auditor
     - Manager
   * - Nonconformities
     - Those they own, detected or follow.
     - All.
     - All.
   * - Corrective and preventive actions
     - Those they own or verify, those of nonconformities they own, and those created from management reviews they
       attend.
     - All.
     - All.
   * - Recurrences
     - All.
     - All.
     - All.
   * - Processes, audit templates and programmes
     - All.
     - All.
     - All.
   * - Audits, checklists and findings
     - Those of the processes they own or work in (as an auditee).
     - All.
     - All.
   * - Controlled documents
     - Those they own, are in the audience of, or wrote a version of.
     - All.
     - All.
   * - Document versions
     - Their own versions while draft or rejected; the effective and obsolete versions of the documents they can see.
     - All.
     - All.
   * - Acknowledgements
     - Their own.
     - All.
     - All.
   * - Management reviews
     - Those they attend, with their inputs and decisions.
     - All.
     - All.
   * - Audit packs
     - None.
     - All.
     - All.
   * - Context issues, interested parties, scope, risks, objectives, satisfaction records, equipment and calibrations
     - All of their companies.
     - All.
     - All.
   * - Competence records, trainings, matrix (Training & Competence)
     - Records and trainings: all; the matrix: the employees they manage; their own under *My competences*.
     - All, and the whole matrix.
     - All, and the whole matrix.
   * - Supplier evaluations, decisions, requirements, SCARs (Supplier evaluation)
     - All.
     - All.
     - All.

"All" means all the records of the companies the person works in; see `Several companies`_. The standards and their
clauses are the same for everyone.

A record's trail and signatures follow the record: whoever can open the record can read them. See :doc:`trail`.

.. tip::
   A quality user who needs to work on a nonconformity they neither own nor detected can be added as a follower in its
   chatter.

Who can do what
===============

The table lists every action of the app. *Yes* means the role can do it on every record it can see; otherwise the
cell says on which records. Items in **QMS Advanced** need the paid layer to be installed.

.. list-table::
   :header-rows: 1
   :widths: 34 22 22 22

   * - Action
     - User
     - Internal auditor
     - Manager
   * - **Nonconformities**
     -
     -
     -
   * - Record a nonconformity
     - Yes
     - Yes
     - Yes
   * - Raise a nonconformity from a receipt, lot, order or repair (see :doc:`sources`)
     - Yes
     - Yes
     - Yes
   * - Edit and accept a new nonconformity
     - Those they own, detected or follow
     - Those they own, detected or follow
     - Yes
   * - Close an open nonconformity (signed)
     - No
     - No
     - Yes
   * - Cancel a new or open nonconformity
     - No
     - No
     - Yes
   * - Amend a closed nonconformity (signed)
     - No
     - No
     - Yes
   * - Delete a new or open nonconformity that carries no signature
     - No
     - No
     - Yes
   * - **Dashboard, clauses and trail**
     -
     -
     -
   * - Open the dashboard
     - Yes, figures of the records they can see
     - Yes
     - Yes
   * - Open the clause view and its evidence
     - Yes, counts of the records they can see
     - Yes
     - Yes
   * - Manage standards and clauses (:menuselection:`Configuration --> Standards`)
     - No
     - No
     - Yes
   * - Verify a record's trail, export it as PDF or CSV
     - Records they can see
     - Records they can see
     - Yes
   * - Export the trail of a period (:menuselection:`Quality --> Evidence --> Trail export`)
     - Rows of the records they can see
     - Rows of the records they can see
     - Yes
   * - **Corrective actions** (QMS Advanced)
     -
     -
     -
   * - Add an action to an open nonconformity
     - Nonconformities they own
     - Nonconformities they own
     - Yes
   * - Start an action, mark it done
     - Actions they own
     - Actions they own
     - Yes
   * - Verify effectiveness (signed)
     - Actions they are the verifier of, never their own
     - Actions they are the verifier of, never their own
     - Any action they do not own
   * - Cancel a draft or in-progress action
     - No
     - No
     - Yes
   * - Amend a verified or ineffective action (signed)
     - No
     - No
     - Yes
   * - Read recurrences
     - Yes
     - Yes
     - Yes
   * - Acknowledge a recurrence
     - No
     - No
     - Yes
   * - **Internal audits** (QMS Advanced)
     -
     -
     -
   * - Manage processes (:menuselection:`Configuration --> Processes`)
     - No
     - No
     - Yes
   * - Manage audit templates (:menuselection:`Configuration --> Audit templates`)
     - No
     - No
     - Yes
   * - Create, approve and close an audit programme
     - No
     - No
     - Yes
   * - Be chosen as lead auditor or co-auditor
     - No
     - Yes
     - Yes
   * - Plan an audit
     - No
     - Audits they lead or co-audit
     - Yes
   * - Start an audit
     - No
     - Audits they lead
     - Yes
   * - Record checklist results and add findings
     - No
     - Audits they lead or co-audit
     - Yes
   * - Report an audit (signed)
     - No
     - Audits they lead
     - Yes, on the lead auditor's behalf
   * - Close a reported audit (findings become nonconformities)
     - No
     - No
     - Yes
   * - Cancel a planned or in-progress audit
     - No
     - No
     - Yes
   * - Amend a reported or closed audit (signed)
     - No
     - No
     - Yes
   * - Print an audit report
     - Audits they can see
     - Yes
     - Yes
   * - **Documents** (QMS Advanced)
     -
     -
     -
   * - Create a document; change its title, owner, audience or clauses
     - No
     - No
     - Yes
   * - Manage document types (:menuselection:`Configuration --> Document types`)
     - No
     - No
     - Yes
   * - Write a new version
     - Documents they can see
     - Yes
     - Yes
   * - Submit, revise or delete a draft version
     - Their own versions
     - Their own versions
     - Yes, on the author's behalf
   * - Approve or reject a version in review (approval signed), by the type's rule
     - As the document's owner, when the rule is *Document owner*
     - As the document's owner, when the rule is *Document owner*
     - Yes (never a version they wrote, never a top-management type)
   * - Approve or reject the quality policy (signed)
     - Only as a member of top management
     - Only as a member of top management
     - Only as a member of top management
   * - Confirm an external document's edition (:guilabel:`Edition still current`); send a copy to an interested party
     - Documents they own (the edition); documents they can see (the copy)
     - Documents they own (the edition); documents they can see (the copy)
     - Yes
   * - Name top management; set retention periods
     - No
     - No
     - Yes
   * - Make an approved version effective today
     - No
     - No
     - Yes
   * - Withdraw an effective or approved version (signed)
     - No
     - No
     - Yes
   * - Amend an effective or obsolete version (signed)
     - No
     - No
     - Yes
   * - List every version (:menuselection:`Resources --> Documents --> Versions`)
     - No
     - Yes
     - Yes
   * - Confirm a periodic review (:guilabel:`Reviewed, no change`)
     - Documents they own
     - Documents they own
     - Yes
   * - Acknowledge a version (:guilabel:`Read and understood`)
     - Their own requests
     - Their own requests
     - Their own requests
   * - See who acknowledged a version
     - Only themselves
     - Yes
     - Yes
   * - Print a controlled copy
     - Versions they can see
     - Yes
     - Yes
   * - Print or export the master list
     - Documents they can see
     - Yes
     - Yes
   * - **Nonconforming output** (free core)
     -
     -
     -
   * - Record and authorise scrap, rework, return to supplier or a hold; record a customer notification
     - Nonconformities they can see
     - Nonconformities they can see
     - Yes
   * - Authorise a regrade, authorise a concession (signed), withdraw a disposition, release a hold, record a waiver
     - No
     - No
     - Yes (a concession never on their own nonconformity)
   * - Declare a clause not applicable, withdraw a declaration
     - No
     - No
     - Yes
   * - **Context, risks, objectives, satisfaction, calibration** (QMS Advanced)
     -
     -
     -
   * - Create and edit context issues, interested parties and needs; record monitoring
     - Yes
     - Yes
     - Yes
   * - Mark an issue reviewed, retire it
     - Issues they own
     - Issues they own
     - Yes
   * - Approve (signed) and revise the scope
     - No
     - No
     - Yes
   * - Record a risk, open it, add treatment actions, re-assess it
     - Risks they own
     - No (read only)
     - Yes
   * - Accept a risk
     - Their own Low or Medium risks
     - No
     - Yes; High and Critical signed
   * - Close a risk
     - No
     - No
     - Yes
   * - Set, activate, close, cancel or continue an objective
     - No
     - No
     - Yes
   * - Record measurements, communicate an objective
     - Objectives they own
     - No (read only)
     - Yes
   * - Record a draft satisfaction result
     - Yes
     - No (read only)
     - Yes
   * - Confirm a satisfaction result, raise an improvement action, record why none is needed
     - No
     - No
     - Yes
   * - Register an instrument, change its calibration settings, retire it
     - No
     - No
     - Yes
   * - Record a calibration and an impact assessment; put an instrument out of service
     - Yes (out of service: instruments they are responsible for)
     - No (read only)
     - Yes
   * - Confirm a calibration
     - Instruments they are responsible for
     - No
     - Yes
   * - Rate the importance of a process; write and amend a programme's rationale
     - No
     - No
     - Yes
   * - **Training & Competence** (add-on)
     -
     -
     -
   * - Manage competences and requirements; plan, mark done or cancel trainings
     - No
     - No
     - Yes
   * - Record an assessment, revoke a record, evaluate a training
     - As the employee's manager
     - As the employee's manager
     - Yes
   * - Record prior experience; grant an auditor qualification (signed)
     - No
     - No
     - Yes
   * - **Supplier evaluation** (add-on)
     -
     -
     -
   * - Run the evaluation, confirm evaluations, score assessments, sign decisions (signed), exempt suppliers
     - No
     - No
     - Yes
   * - Record a draft requirement; request and send a SCAR, record the supplier's response
     - Yes
     - Requirements: no; SCARs: yes
     - Yes
   * - Communicate, supersede or withdraw a requirement
     - No
     - No
     - Yes
   * - Confirm a purchase order anyway, with a reason (control *Warn*)
     - As a Purchase user
     - As a Purchase user
     - As a Purchase user
   * - **Management reviews** (QMS Advanced)
     -
     -
     -
   * - Chair a management review
     - No
     - No
     - Yes
   * - Create a review, edit it, recompute its inputs, record decisions and the conclusion
     - No
     - No
     - Yes
   * - Hold the review
     - No
     - No
     - Yes, as the chair or on the chair's behalf
   * - Create an action from a decision
     - No
     - No
     - Yes
   * - Approve the review (signed)
     - No
     - No
     - Only the chair
   * - Update the status of a decision of an approved review
     - No
     - No
     - Yes
   * - Amend the conclusion of an approved review (signed)
     - No
     - No
     - Yes
   * - Print the minutes of a held or approved review
     - Reviews they attend
     - Yes
     - Yes
   * - **Audit pack** (QMS Advanced)
     -
     -
     -
   * - Open packs, preview and download the ZIP and its files
     - No
     - Yes
     - Yes
   * - Request a pack, print the clause matrix
     - No
     - Yes
     - Yes
   * - Cancel a queued pack
     - No
     - Packs they requested
     - Yes
   * - Delete a failed or cancelled pack
     - No
     - No
     - Yes
   * - **Settings**
     -
     -
     -
   * - Change the Quality settings (:menuselection:`Settings --> Quality`)
     - No
     - No
     - Yes, with the *Administration: Settings* right

.. note::
   Buttons are shown only to the people who can use them. For example, :guilabel:`Start` and :guilabel:`Mark done` on
   a corrective action are shown to its owner and to quality managers; :guilabel:`Start` and :guilabel:`Report` on an
   audit to its lead auditor and to quality managers, not to co-auditors; :guilabel:`Submit` and :guilabel:`Revise` on
   a document version to its author and to quality managers.

   On the registers whose buttons belong to a named person — risks, environmental aspects, hazards, legal
   requirements, monitoring indicators, emergency situations, incidents and consultations — a blue line under the
   header of a record you cannot act on says who can, for example *Only the owner (DEMO Operations Manager) or a
   quality manager can work on this hazard.* Internal auditors read *Auditors have read-only access.*

   When a save would set a value that only a button may set, a window explains what happened, what was kept of your
   edit and, if you may press the button, offers it (for example :guilabel:`Accept now…`); otherwise it names who can.
   :guilabel:`Got it` closes it.

.. important::
   - Only users with the :guilabel:`Internal auditor` or :guilabel:`Manager` role can be chosen as lead auditor or
     co-auditor. See :doc:`audits`.
   - The chair of a management review must be a quality manager. See :doc:`management_reviews`.
   - The *Approve* to-do of a new document version goes to the people the document type names — the owner, the
     quality managers or top management — never to its author. See :doc:`documents`.
   - With the Training & Competence add-on, the lead auditor of an audit must be qualified for the audit to start. See
     :doc:`competence`.

Environment, health and safety
==============================

With the environment, health and safety registers switched on (see :doc:`ehs_setup`), the three Quality roles work on
them as on the other registers, with these particulars:

.. list-table::
   :header-rows: 1
   :widths: 34 22 22 22

   * - Action
     - User
     - Internal auditor
     - Manager
   * - Read the EHS registers of the standards switched on
     - Yes
     - Yes
     - Yes
   * - Record obligations, situations, indicators, readings, aspects, hazards, consultations
     - Yes
     - No
     - Yes
   * - Activate, open, re-assess, record drills, triage reports
     - As the owner, responsible, coordinator or organiser (triage: any quality user)
     - No
     - Yes
   * - Withdraw an obligation, retire a situation, override an aspect's significance, close an aspect, a hazard or an
       incident, decide reportability
     - No
     - No
     - Yes
   * - Read and write the injury details of an incident
     - No
     - No
     - Yes
   * - See who sent a confidential worker hazard report
     - No
     - No
     - Yes
   * - Report an incident from Safety reports
     - Yes
     - No
     - Yes
   * - Report a hazard from Safety reports
     - Yes
     - Yes
     - Yes

Employees without a Quality role see only the **Safety reports** app: they report incidents and hazards and read their
own reports, nothing else. Portal users see neither. Switching the registers on changes no user's type in Odoo.

Separation of duties
====================

ISO management systems expect that nobody checks their own work. The app enforces it in these places, for quality
managers too:

Author and approver
   The author of a document version can never approve it, even when they are a quality manager. The
   :guilabel:`Approve` button is hidden from them; the owner, a quality manager or top management approves, by the
   document type's rule. See :doc:`documents`.

Concessions
   A repair or use-as-is disposition is authorised by a quality manager other than the nonconformity's owner. See
   :doc:`nonconformities`.

Assessor and employee
   Nobody assesses their own competence, and nobody evaluates their own training; the trainer does not either. See
   :doc:`competence`.

Owner and verifier
   The verifier of a corrective action cannot be its owner, and the owner can never sign the effectiveness verdict,
   even as a quality manager: the :guilabel:`Verify` button is hidden from them. See :doc:`corrective_actions`.

Auditor independence
   The lead auditor and the co-auditors of an audit cannot be the owner of the audited process or one of its auditees.
   Odoo refuses to save such an audit, and checks again when the audit starts. The rule applies to quality managers
   too. See :doc:`audits`.

The chair approves the review
   Only the chair of a management review can approve it. A quality manager who is not the chair cannot approve it,
   even on the chair's behalf. See :doc:`management_reviews`.

Some actions can be done by a quality manager *on behalf of* the person they belong to: submitting a document version
for its author, reporting an audit for its lead auditor, holding a review for its chair. The trail then records that
it was done on their behalf.

Nobody, not even a quality manager, can acknowledge a document for someone else.

Signatures and the password re-check
====================================

These decisions are electronic signatures: closing a nonconformity, authorising a concession, amending a locked record
and, with QMS Advanced, signing the effectiveness verdict of an action, reporting an audit, approving a document version
or accepting an external document for use, withdrawing a document version, approving a management review, approving
the scope and accepting a high or critical risk; with the add-ons, granting an auditor qualification and signing a
supplier decision. Each signature records who signed, when, why, and the
fingerprint of the record at that moment. See :doc:`trail`.

By default, Odoo asks the signer for their own password before signing, in its standard *confirm your password*
dialog, so that nobody can sign from someone else's unattended session. Odoo does not ask again if the person
confirmed their password in the last ten minutes.

A quality manager can turn the password request off with :ref:`Ask the password before signing <config-password>`,
for example where people sign in through single sign-on and have no Odoo password. The decisions are still signed,
without the password check, and every change of this setting is recorded in the trail.

Several companies
=================

On a database with several companies, quality records belong to a company:

- a nonconformity, audit, programme, process, audit template, document, management review or audit pack takes the
  company you are working in when it is created; a nonconformity raised from an operation takes the company of that
  operation;
- corrective actions, checklist lines, findings, document versions, acknowledgements and recurrences take the company
  of the record they belong to;
- numbers run per company: two companies each have their own ``NC/2026/00001``.

People see and work on the records of the companies selected in the company switcher at the top of the screen, and
their role applies in each of those companies. This holds for quality managers too, including the trail: a quality
manager reads the trail rows of the records of their own companies only, in searches and in the period export.
Reminders that go to "the quality managers" go to the quality managers
who have access to the record's company.

Some things are shared by every company:

- the standards and their clauses;
- the Quality settings, which are the same for the whole database;
- document types whose :guilabel:`Company` is left empty.

An audit pack covers the company you are working in when you request it. See :doc:`audit_pack`.

.. seealso::
   - :doc:`configuration`
   - :doc:`nonconformities`
   - :doc:`trail`
   - :doc:`faq`

========
Glossary
========

The words below are used throughout the **Quality** guide with the meaning given here.

.. glossary::

   5 Whys
      A root-cause method that asks *why?* again and again until the underlying cause is reached. See
      :doc:`nonconformities`.

   Accept
      The step that moves a nonconformity from **New** to **Open**, setting its severity, owner, due date and clauses.
      See :doc:`nonconformities`.

   Acceptance for use
      The signed approval of a document of external origin: the person who may approve it confirms that the issuer's
      edition can be used. See :doc:`documents`.

   Acknowledgement
      Also *read and understood*. A reader's own confirmation, after opening the file, that they read and understood a
      document version in force. Nobody can acknowledge for someone else. See :doc:`documents`.

   Acknowledgement grace
      The number of days (14 by default) a reader has to acknowledge a new document version before the acknowledgement
      is overdue. See :doc:`documents`.

   Action expected
      The flag set on a confirmed satisfaction record that was below its target or dropped by at least the deterioration
      threshold; it stays until an improvement action is raised or a quality manager records why none is needed. See
      :doc:`satisfaction`.

   Ad hoc audit
      An audit that belongs to no programme, for example one decided after a customer complaint. It does not count in
      any programme's completion. See :doc:`audits`.

   Adjustment protection
      How a measuring instrument is protected from adjustments that would invalidate its calibration: a seal, a locked
      setting or a password. It is checked at every calibration. See :doc:`calibration`.

   Age bucket
      A range of days since detection used by the *Open nonconformities by age* tile of the dashboard (by default 0-30,
      31-60, 61-90 and over 90 days). See :doc:`dashboard`.

   Amendment
      A signed correction, with a reason, of a locked record: a closed nonconformity and, with QMS Advanced, a verified or
      ineffective action, a reported or closed audit, a version in force or obsolete, or an approved review. Only
      the fields each record allows can be amended. The trail keeps the original value next to the new one. See
      :doc:`trail`.

   Approved supplier list
      The suppliers a company may buy from, kept by signed decisions: each supplier is Approved, Conditional, Blocked,
      Unapproved (no decision) or Exempt. See :doc:`suppliers`.

   Area
      Two to four capital letters for the department a document belongs to, for example ``PUR``; the middle part of
      the document code. ``GEN`` when left empty. See :doc:`documents`.

   Audience
      The users, named or through user groups, who must read a controlled document. See :doc:`documents`.

   Audit
      Here, an internal audit: the check of one process against the clauses in its scope, planned for a month, run by
      a lead auditor with a checklist, reported with a signature and closed by a quality manager. See :doc:`audits`.

   Audit pack
      One ZIP file, built by the app for a chosen period, holding the evidence an external auditor asks for: the
      nonconformity log, the status of the actions, the audit reports, the document master list, the acknowledgement
      matrix, the review minutes, the registers of context, risks, objectives, calibration and satisfaction (and, with
      the add-ons, competence and the approved supplier list), the clause matrix and the integrity and completeness
      report. Every file is dated and fingerprinted. See :doc:`audit_pack`.

   Audit programme
      The plan of a year's internal audits, one per year and company, approved by a quality manager and closed at the
      end of the year. See :doc:`audits`.

   Audit template
      A reusable checklist: a list of audit questions, each tied to a clause. See :doc:`audits`.

   Auditee
      A user who works in a process. Neither the auditees nor the process owner may audit that process. See
      :doc:`audits`.

   Auditor qualification
      The internal auditor competence (ISO 19011) of a person, granted as a signed competence record: level 2 audits,
      level 3 leads an audit, by default. With the Training & Competence add-on, an audit whose lead auditor is not
      qualified cannot start. See :doc:`competence`.

   Awaiting verdict
      Said of a **Done** corrective action whose effectiveness date has arrived and that has no verdict yet. See
      :doc:`corrective_actions`.

   Bundle hash
      The single SHA-256 fingerprint shown on a done audit pack, computed from the SHA-256 values of all its files. It
      is not the fingerprint of the ZIP file itself. See :doc:`audit_pack`.

   Cause category
      The family of a root cause: Man, Machine, Method, Material, Measurement or Environment. It is used to detect
      recurrences. See :doc:`corrective_actions`.

   Chair
      The member of top management who chairs a management review and is the only one who can approve it. The chair
      must be a quality manager. See :doc:`management_reviews`.

   Change summary
      What changed in a document version compared with the previous one. It is required to submit a version. See
      :doc:`documents`.

   Clause
      A numbered requirement of a standard, such as *9001 · 10.2*. Clauses form a tree: ``10.2`` sits under ``10``.
      See :doc:`clauses`.

   Clause applicability
      The declaration, by a quality manager and with a justification, that a clause does not apply to a company; see
      *Not applicable*. See :doc:`clauses`.

   Clause matrix
      A PDF listing, for each clause of the chosen standards, the evidence count in a period and the count per type of
      record, with the clauses without evidence highlighted. It is part of the audit pack and can be printed on its
      own. See :doc:`audit_pack`.

   Closure blocker
      Something still missing before a nonconformity can close, such as the containment, the correction, the root
      cause, a clause, the owner's activity or, with QMS Advanced, a corrective action to verify. See
      :doc:`nonconformities`.

   Co-auditor
      An additional auditor on an audit, who records checklist results and findings but cannot start or report the
      audit. Like the lead auditor, a co-auditor holds the Internal auditor role. See :doc:`audits`.

   Competence
      An ability the company needs, such as *CMM measurement*, with its category, its validity and the words of its three
      levels. See :doc:`competence`.

   Competence matrix
      The table of employees against the competences required or held, each cell reading OK, Expiring or Gap. It never
      shows document acknowledgements. See :doc:`competence`.

   Competence record
      The evidence that an employee holds a competence at a level from a date until an expiry: from a passed training,
      an assessment, prior education or experience, or a signed qualification. Never edited in substance and never
      deleted: superseded or revoked. See :doc:`competence`.

   Completeness checks
      The eleven questions the integrity and completeness report of an audit pack asks of the period's records, for
      example closed nonconformities without a root cause, or verified actions without evidence. Each lists the
      records concerned. See :doc:`audit_pack`.

   Concession
      A disposition that lets nonconforming output go on — *Repair* or *Use as is* — authorised with a signature by a
      quality manager other than the nonconformity's owner, possibly with the customer's approval reference. See
      :doc:`nonconformities`.

   Conclusion
      The overall result of an audit, chosen when it is reported: *Conforming*, *Conforming with findings* or *Not
      conforming*. It must agree with the grades of the findings. Management reviews also end with a written
      conclusion. See :doc:`audits`.

   Containment
      The immediate action that stopped a problem from spreading, such as quarantining a batch. See
      :doc:`nonconformities`.

   Context issue
      An internal or external issue that affects the results of the quality system (ISO 9001 4.1), with an owner, an
      effect and a review date. See :doc:`context`.

   Controlled copy
      A PDF of a document version with a stamp on every page stating its status (*CONTROLLED COPY*, *DRAFT — NOT FOR
      USE*, *APPROVED — EFFECTIVE FROM …*, *OBSOLETE — SUPERSEDED …*) and its reference. See :doc:`documents`.

   Controlled document
      A procedure, work instruction, form, policy or manual whose versions are approved before use, kept with their
      effective dates and reviewed periodically (ISO 9001 clause 7.5). See :doc:`documents`.

   Correction
      What was done to fix the nonconforming item itself, as opposed to a corrective action, which removes its cause.
      See :doc:`nonconformities`.

   Corrective action
      An action that removes the cause of a nonconformity so that it does not happen again. Its effectiveness is
      verified and signed by someone other than its owner. See :doc:`corrective_actions`.

   Customer notification
      The record that a customer was told that nonconforming output may have reached them: who, when, how and what was
      said. See :doc:`nonconformities`.

   Deviation
      A difference between an audit programme and the proposed audit frequency: a process due without an audit planned,
      or planned later than proposed. The rationale of the programme explains it. See :doc:`audits`.

   Disposition
      What is done with nonconforming output, for a quantity: scrap, rework, repair, use as is, regrade, return to
      supplier, or a hold. Each line is authorised; the lines must cover the quantity affected before closing. See
      :doc:`nonconformities`.

   Do not use
      The flag of a measuring instrument that may not be used today: overdue, out of tolerance, never calibrated, out of
      service or retired. See :doc:`calibration`.

   Document code
      The identifier of a controlled document, made of the type prefix, the area and a number, for example
      ``PRO-QUA-001``. It is given when the document is created and never changes. See :doc:`documents`.

   Document hash
      The fingerprint printed in the footer of a Quality report, such as a trail PDF. It lets a printed copy be matched
      to the document that was generated. See :doc:`trail`.

   Document type
      The kind of a controlled document (Procedure, Work instruction, Form, Policy, Manual…), with its code prefix, its
      review period and whether readers must acknowledge it. See :doc:`documents`.

   Document version
      One numbered revision of a controlled document (v1, v2…), with its file, change summary, author, approver and
      effective dates. See :doc:`documents`.

   Edition check
      The periodic check, 12 months by default, that the edition of an external document in use is still the issuer's
      current one. See :doc:`documents`.

   Effective from
   Effective until
      The window in which a document version is in force: from the first date, included, to the second, excluded. See
      :doc:`documents`.

   Effectiveness date
      The first day on which the effect of a corrective action can be judged. It is at least the effectiveness gap
      (30 days by default) after the action's due date. See :doc:`corrective_actions`.

   Effectiveness verdict
      The signed judgement that a corrective action worked (*Effective*) or did not (*Ineffective*), given by someone
      other than the action's owner. See :doc:`corrective_actions`.

   Electronic signature
      A record of who approved what, when and why, together with the fingerprint of the record at that moment. By
      default it requires the signer's password. See :doc:`trail`.

   Enabled standard
      A standard whose clauses are offered when tagging records. Standards are enabled in the Quality settings. See
      :doc:`clauses`.

   Evidence
      The quality records tagged with a clause. The clause view counts them for a period. See :doc:`clauses`.

   Evidence span
      The time a record stays in force — a document version from its effective date until it is replaced, a risk from its
      identification until its closure, a declaration while it is in force. The record counts in the clause view in every
      period its evidence span overlaps. See :doc:`clauses`.

   External document
      A document written elsewhere — a standard, a customer drawing — controlled with its issuer, reference and edition,
      and accepted for use rather than approved. See :doc:`documents`.

   Fallback owner
      The user who receives the reminders and to-dos meant for an owner whose user has been deactivated, and the
      nonconformities of a closed audit when the process owner is archived. When none is set, the first quality
      manager of the company receives them. See :doc:`configuration`.

   File SHA-1
      The fingerprint of a document version's file, taken at upload. Any later change to the file is detected against
      it. See :doc:`documents`.

   Finding
      What an audit found, graded *Observation*, *Minor* or *Major*. Minor and major findings become nonconformities
      when the audit is closed. See :doc:`audits`.

   Gap
      A clause of an enabled standard with no evidence in the chosen period. See :doc:`clauses`.

   Hash
      A 64-character fingerprint of a trail row, computed from its content and from the previous row's hash, so that
      any later change breaks the chain. See :doc:`trail`.

   Hash chain
      The rows of a record's trail linked together by their hashes. :guilabel:`Verify trail` checks it. See
      :doc:`trail`.

   Hold
      The disposition *Suspend provision (hold)*: the provision of nonconforming output is stopped until a quality manager
      releases it, once a final disposition is authorised. See :doc:`nonconformities`.

   Impact assessment
      After a calibration finds an instrument out of tolerance, the record of what was measured with it since its last
      good calibration and the conclusion; the linked nonconformity cannot close without it. See :doc:`calibration`.

   Importance
      The rating of a process — High, Medium or Low — that sets the base interval of its proposed audit frequency. See
      :doc:`audits`.

   Interested party
      A person or group that affects or is affected by the quality system (ISO 9001 4.2), with its needs and
      expectations and how each is monitored. See :doc:`context`.

   Internal auditor
      The Quality role for people who must read the whole quality system and run internal audits. It includes the
      User role. See :doc:`roles`.

   Ishikawa
      A root-cause method, also called the fishbone diagram, that sorts possible causes into families. See
      :doc:`nonconformities`.

   Keep until
      The date until which a record must be kept, computed from the retention period of its record type once it stops
      being live. Past that date the record is *past retention*; nothing is deleted automatically. See
      :doc:`documents`.

   Late audit
      An audit still **Planned** after its planned month has ended. See :doc:`audits`.

   Lead auditor
      The auditor responsible for an audit, and the only one who starts and reports it (a quality manager can do it on
      their behalf). Holds the Internal auditor role. See :doc:`audits`.

   Locked record
      A record in a final state, such as a closed or cancelled nonconformity. Its content can no longer be changed,
      only amended, and it cannot be deleted. See :doc:`trail`.

   Management review
      Top management's review of the quality management system at planned intervals (ISO 9001 clause 9.3), with its
      inputs, decisions and signed minutes. See :doc:`management_reviews`.

   Manifest
      The ``manifest.json`` file of an audit pack: the pack's number, period, standards, requester and generation time,
      and each file's size, SHA-256 and record count. See :doc:`audit_pack`.

   Master list
      The list of all controlled documents with, for a chosen date, the version in force, its effective date, the next
      review, the audience and the acknowledgement completion. See :doc:`documents`.

   Minutes hash
      The fingerprint of a management review's trail at the moment the chair approved it, printed on the minutes. See
      :doc:`management_reviews`.

   Nonconformity
      Also *NC*. Anything that did not meet a requirement: a complaint, a supplier defect, an inspection failure, an
      audit finding, a health and safety event or an internal problem. See :doc:`nonconformities`.

   Not applicable
      A clause declared not applicable to a company, with its justification, from a date: it and its sub-clauses read *Not
      applicable* in the clause view and are not gaps. Clauses of sections 4 and 5 can never be. See :doc:`clauses`.

   Objective evidence
      The records, samples or observations that support an audit finding. See :doc:`audits`.

   Observation
      A finding that is not a nonconformity: a weakness or an improvement opportunity. It stays in the audit report
      and creates no nonconformity. See :doc:`audits`.

   Overdue
      Said of a new or open nonconformity whose due date has passed, and of a corrective action still **In progress**
      after its due date. See :doc:`nonconformities` and :doc:`corrective_actions`.

   Owner
      The internal user responsible for a record: for a nonconformity, the person who treats it by its due date; for a
      corrective action, the person who carries it out; for a document, the person responsible for it and its periodic
      review. See :doc:`nonconformities`.

   Password re-check
      Odoo's *confirm your password* dialog shown before a signature, so that nobody signs from someone else's
      session. It is not shown again within ten minutes of the last confirmation, and can be turned off in the
      settings. See :doc:`trail`.

   Periodic assessment
      The evaluation of a service or outsourced-process provider by criteria scored 0 to 5, at an interval, instead of
      the rating from receipts. See :doc:`suppliers`.

   Periodic review
      The owner's regular check that a document is still right. Its next date follows from the effective date and the
      review period of the document type. See :doc:`documents`.

   Portal reader
      A person without an internal user, named on a controlled document, who reads and acknowledges its version in force
      in the My Account portal and sees nothing else of the app. See :doc:`documents`.

   Preventive action
      An action on a potential cause, before any nonconformity happened. It is tracked and verified like a corrective
      action but never required to close a nonconformity. Actions created from management review decisions are
      preventive. See :doc:`corrective_actions`.

   Process
      One process of the management system, such as *Purchasing* or *Production*, with its owner, its auditees and its
      realised clauses. Each audit audits one process. See :doc:`audits`.

   Process owner
      The user responsible for a process. They may not audit it, and they own the nonconformities raised from its audit
      findings. See :doc:`audits`.

   Process register
      The list of the processes of the management system, in :menuselection:`Quality --> Configuration --> Processes`.
      See :doc:`audits`.

   Programme completion
      The closed audits of a programme divided by its audits that are not cancelled. See :doc:`audits`.

   Proposed audit frequency
      The interval Odoo proposes between two audits of a process, from its importance and factors for past findings,
      changes and nonconformities. A proposal, never an automatic audit. See :doc:`audits`.

   QMS Advanced
      The paid layer of the Quality app. It adds corrective actions, internal audits, document control, management
      reviews and the audit pack to the free core. See :doc:`configuration`.

   QMS scope
      The scope of the quality system (ISO 9001 4.3), approved with a signature as a numbered version in force until it is
      revised, with the clauses declared not applicable frozen with it. See :doc:`context`.

   Quality manager
      The Quality role for the people who run the quality system: they close, cancel and amend records, approve
      documents, close audits and change the settings. It includes the Internal auditor role. See :doc:`roles`.

   Quality objective
      A measurable objective with a target, a period, an owner and its 6.2.2 plan, activated by a quality manager and
      closed with its result. See :doc:`objectives`.

   Quality policy
      The policy of the company (ISO 9001 5.2), one in force per company, approved by top management with the four 5.2.1
      confirmations and read by everyone of the company. See :doc:`documents`.

   Quality user
      The Quality role for people who raise and treat nonconformities, carry out actions and read documents. See
      :doc:`roles`.

   Rationale
      The written reason of an audit programme — why these processes, in these months — required to approve it and frozen
      with its proposal. See :doc:`audits`.

   Re-assessment
      A new scoring of an open risk after treatment, at its periodic review or after a change, recorded with the previous
      score and the change. See :doc:`risks`.

   Realised clauses
      The clauses of a standard that a process carries out. They are the default scope of its audits. See
      :doc:`audits`.

   Receipt measures
      The on-time rate and the quantity rate of a supplier, counted from the receipts of a period. They need Inventory.
      See :doc:`suppliers`.

   Record hash
      The trail head hash stored in a signature: the proof of which version of the record was signed. See
      :doc:`trail`.

   Recurrence
      A nonconformity that, when accepted, repeats an earlier one of the same company detected within the recurrence
      window: same product, same process, or same cause category from the same source type. See
      :doc:`corrective_actions`.

   Recurrence window
      How many days back Odoo looks for an earlier matching nonconformity when one is accepted (180 by default; 0
      switches detection off). See :doc:`corrective_actions`.

   Report hash
      The fingerprint of an audit's trail at the moment the lead auditor signed the report. See :doc:`audits`.

   Retention period
      How many years a type of record is kept once it stops being live, set per record type and company, 5 years by
      default. See :doc:`documents`.

   Review decision
      An output of a management review (ISO 9001 clause 9.3.3): an improvement, a resource, a change to the QMS, an
      action or another decision, with an owner and a due date. See :doc:`management_reviews`.

   Review input
      One agenda item of a management review, from the list of ISO 9001 clause 9.3.2, with its computed figures, notes
      and a *Discussed* switch. See :doc:`management_reviews`.

   Review interval
      The number of months (12 by default) between two management reviews. The next review is due that long after the
      meeting of the last approved one. See :doc:`management_reviews`.

   Risk level
      Low, Medium, High or Critical, from the score likelihood × severity and the company's thresholds (5, 10 and 15 by
      default). See :doc:`risks`.

   Root cause
      Why a nonconformity happened, recorded with the method used (5 Whys, Ishikawa or Other). See
      :doc:`nonconformities`.

   Root cause to revisit
      The flag set on a nonconformity when one of its corrective actions is judged ineffective, or when the problem
      came back after it was closed. It blocks closure until the root cause is changed and a new corrective action is
      started. See :doc:`corrective_actions`.

   SCAR
      Supplier corrective action request: a corrective action asked of a supplier from a supplier nonconformity, sent to
      their contact, and done only once the supplier's response is recorded. See :doc:`suppliers`.

   Scope
      Of an audit: the clauses an audit covers, and a description of what else it covers (sites, shifts, products). By default the
      realised clauses of the audited process. See :doc:`audits`. For the scope of the quality system, see *QMS
      scope*.

   Severity
      How serious a nonconformity is: *Minor*, *Major* or *Critical*. With QMS Advanced, major and critical
      nonconformities need a verified corrective action before closing, by default. See :doc:`nonconformities`.

   Source description
      A summary of the record a nonconformity was raised from, kept on the nonconformity and readable even if that
      record is later deleted or restricted. See :doc:`sources`.

   Source modules
      Free modules that add the *Raise nonconformity* button to Inventory, Manufacturing, Purchase and Repairs records,
      and the product and lot fields to nonconformities. They install themselves. See :doc:`sources`.

   Source record
      The record a nonconformity was raised from: a transfer, a lot, a manufacturing order, a work order, a purchase
      order, a repair or an audit finding. See :doc:`sources`.

   Source type
      Where a nonconformity comes from: Audit, Complaint, Inspection, Supplier, Internal, or Health, safety and
      environment. The list is fixed so that statistics compare across sites. See :doc:`nonconformities`.

   Standard
      A management-system standard, such as ISO 9001, whose clauses can be tagged on quality records. See
      :doc:`clauses`.

   Supersession
      A new document version coming into force makes the previous one obsolete on the same day, and also an older
      approved version still waiting for its date. See :doc:`documents`.

   Supplier decision
      The signed decision that puts a supplier on the approved supplier list as Approved, Conditional or Blocked, with a
      reason and a re-evaluation date. See :doc:`suppliers`.

   Supplier evaluation
      The rating of a supplier for a period: a score from 0 to 100, a grade A to D and a proposed status, from its receipts
      and supplier nonconformities or from a periodic assessment. See :doc:`suppliers`.

   Time cap
      The number of seconds (600 by default) after which a generating audit pack fails with *timeout*. See
      :doc:`audit_pack`.

   Top management
      The members of a company's top management named in the Quality settings; they approve the quality policy and need
      no Quality role. See :doc:`documents`.

   Trail
      The list of everything that happened to a quality record — creation, state and field changes, signatures,
      amendments — which nobody can edit or delete. See :doc:`trail`.

   Trail head hash
      The hash of the latest trail row of a record: the fingerprint of the record's whole history so far. See
      :doc:`trail`.

   Trail integrity report
      The part of an audit pack that verifies the trail of every record the pack covers and names each record whose
      trail is broken. See :doc:`audit_pack`.

   Treatment
      The decision on a risk — reduce, avoid, transfer or accept — or on an opportunity — pursue or decline. See
      :doc:`risks`.

   Verifier
      The person who signs the effectiveness verdict of a corrective action. It is never the action's owner. See
      :doc:`corrective_actions`.

   Version in force
      The effective version of a document on a given date. There is never more than one. See :doc:`documents`.

   Waiver
      A quality manager's written reason why no customer needs to be informed of nonconforming output that may have
      reached them. See :doc:`nonconformities`.

   Withdrawal
      Taking an effective document version out of use without a replacement, signed by a quality manager with a
      reason. See :doc:`documents`.

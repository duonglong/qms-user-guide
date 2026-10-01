=============================
Questions and troubleshooting
=============================

The answers below cover the questions and messages people meet most often. Each one links to the page that explains
the feature in full.

Nonconformities
===============

**Why can't I close this nonconformity?**
   Odoo lists what is missing: the containment, the correction, the root cause, at least one clause, or the owner's
   *Nonconformity to treat* activity (mark it done in the chatter). The yellow banner *N items before closure* on the
   form gives the count. Only a quality manager can close, and only an **Open** nonconformity: accept a new one first.
   With QMS Advanced, the corrective actions are checked too. See :doc:`nonconformities` and :doc:`corrective_actions`.

**I don't see the Close, Cancel or Amend button.**
   These buttons are reserved to quality managers. :guilabel:`Close` shows on open nonconformities only,
   :guilabel:`Cancel` on new and open ones, :guilabel:`Amend` on closed ones. See :doc:`nonconformities`.

**How do I correct a signed audit report, an approved review, a verdict's wording or a version in force?**
   With QMS Advanced, a quality manager clicks :guilabel:`Amend` on the locked record, changes the fields it allows and
   gives a reason; the amendment is signed and the trail keeps both values. See :doc:`trail`.

**Odoo says "Tag at least one clause before Open."**
   A nonconformity cannot be accepted, or stay open, without a clause. Tag one in the :guilabel:`Accept` dialog or on
   the :guilabel:`Clauses` tab. See :doc:`clauses`.

**Odoo says "This record is locked; use Amend."**
   The nonconformity is closed or cancelled. A quality manager can amend a closed one — title, treatment, root cause
   method, source description and clauses — with a reason. A cancelled nonconformity cannot be amended. See
   :ref:`Cancel or amend <nc-cancel-amend>`.

**I clicked Amend and sign, but the Amendment Count did not change.**
   Only the fields you actually changed are amended: when nothing differs from the closed record, nothing is
   recorded. When Odoo asks for your password, the amendment is applied only after you confirm it; if you discard the
   password dialog, nothing is changed. See :ref:`Cancel or amend <nc-cancel-amend>`.

**Why was I not asked for my password when closing?**
   Odoo does not ask again within ten minutes of your last password confirmation, and a manager may have turned off
   :guilabel:`Ask the password before signing`. The closure is signed either way. See :doc:`trail`.

**A quality user cannot see a nonconformity a colleague raised.**
   Quality users see only the nonconformities they own, detected or follow. Add them as a follower in the chatter, or
   give them the :guilabel:`Internal auditor` role to read every nonconformity. See :doc:`roles`.

**Can I delete a nonconformity?**
   A quality manager can delete a new or open nonconformity that carries no signature. Closed and cancelled
   nonconformities can never be deleted. To remove a duplicate from the register, cancel it with a reason instead:
   its number is kept. See :doc:`nonconformities`.

**Close lists "Record the disposition of the nonconforming output" or "Dispose of the whole affected quantity".**
   The nonconformity concerns an output: add disposition lines on the :guilabel:`Disposition` tab until they cover the
   :guilabel:`Quantity affected` (a hold does not count), then authorise each line. See :ref:`nc-disposition`.

**Odoo says "Only a quality manager can decide that this nonconformity concerns no output."**
   Inspection, supplier and complaint nonconformities start with :guilabel:`Disposition required` ticked. Only a
   quality manager can untick it. See :ref:`nc-disposition`.

**Authorise refuses: "A concession is authorised by a quality manager other than the nonconformity owner."**
   Repair and use as is are concessions: another quality manager authorises them, with a signature. When the setting
   requires it, record the customer's approval reference first (*Record the customer's approval reference for this
   concession.*). See :ref:`nc-disposition`.

**Odoo says "An authorised disposition cannot change: withdraw it and record a new line."**
   An authorised line is final. A quality manager withdraws it with a reason, and a new line is recorded. A disposition
   is never deleted. See :ref:`nc-disposition`.

**Close lists "Record that the customer was informed, or why not".**
   :guilabel:`Reached a customer` is *Possibly* or *Yes*: record a customer notification on the :guilabel:`Customers
   informed` tab, or have a quality manager write why no customer is informed. See :ref:`nc-customer`.

**Release refuses: "Record what is done with the held output before releasing it."**
   A hold is lifted only once a final disposition is authorised. While a hold is authorised, the nonconformity cannot
   close (*Release or replace the hold on the output*). See :ref:`nc-hold`.

Operations
==========

**The Raise nonconformity button is missing on a receipt or an order.**
   The user needs a Quality role, and the source module for that app must be installed. Each source module installs
   itself when both the Quality app and the app it connects to are installed. See :doc:`sources`.

**I cannot change the Source Type of a nonconformity raised from a receipt.**
   A nonconformity raised from a record keeps the source type that record gives it. To record the problem under
   another source type, create the nonconformity from :menuselection:`Quality --> Nonconformities --> Nonconformities`. See
   :doc:`sources`.

**Why is the Product field empty on a nonconformity raised from a receipt?**
   The product and the lot are filled in only when the record involves exactly one product or one lot. When there are
   several, the source description names up to three products. See :doc:`sources`.

**The Nonconformities smart button shows a lower count for me than for my manager.**
   The count includes only the nonconformities you are allowed to see, and never cancelled ones. See :doc:`sources`.

Dashboard
=========

**The dashboard figures differ between two people.**
   Every tile counts only the records the viewer is allowed to see. :guilabel:`My records` narrows it further to the
   records they own. See :doc:`dashboard`.

**A dashboard tile shows "?".**
   That tile could not be computed; the other tiles still work. Reload the page, and tell your administrator if it
   persists. See :doc:`dashboard`.

Clauses
=======

**Why does a clause show a gap although I have evidence?**
   The evidence must fall in the chosen period (for a nonconformity, its :guilabel:`Detected On` date), must not be
   cancelled, and must be visible to you. Widen the period or check the record's clause tags. See :doc:`clauses`.

**Why does the clause view say "Records tagged" and not "evidence"?**
   Records tagged to a clause show where to look. They are not proof of conformity: conformity is judged against the
   requirement. See :doc:`clauses`.

**A procedure approved two years ago counts in this quarter. Is that right?**
   Yes. A record in force — a document version, a process, a risk, an objective — counts in every period its time in
   force overlaps. See :doc:`clauses`.

**Mark not applicable refuses: "Clauses of sections … apply to every organization."**
   Sections 4 and 5 can never be declared not applicable, and each standard lists the sections that may be. See
   :ref:`clauses-not-applicable`.

**Odoo says "<clause> already covers <sub-clause>" or "… is already declared not applicable for …".**
   The clause, or its parent, is already declared for that company. Withdraw the declaration first if it must change.
   See :ref:`clauses-not-applicable`.

**I withdrew a declaration but last quarter still shows the clause "Not applicable".**
   That is intended: the clause view reads the declarations as they stood on the last day of the chosen period. See
   :ref:`clauses-not-applicable`.

**I enabled a standard in Configuration ‣ Standards, but it switched off again.**
   Enable standards in :menuselection:`Settings --> Quality`: saving the settings applies the list of enabled
   standards and switches off any standard not in it. See :doc:`clauses`.

Trail and signatures
====================

**The trail PDF export is refused.**
   The export has more rows than the :guilabel:`Trail PDF row limit` (5,000 by default). Shorten the period, or use the
   CSV export, which has no limit. See :doc:`trail`.

**Verify trail says "Trail broken at row K".**
   The database was changed outside Odoo. Do not try to correct it: export the trail as it is and inform your quality
   manager and your system administrator. See :doc:`trail`.

**Can I turn off the password request for signatures?**
   Yes, a quality manager can untick :guilabel:`Ask the password before signing` in :menuselection:`Settings -->
   Quality`. Do so only when people sign in through single sign-on and have no Odoo password. The change is recorded
   in the trail. See :doc:`configuration`.

Corrective actions
==================

**I cannot add a corrective action to a nonconformity.**
   The nonconformity must be accepted (**Open**) first, and a closed one takes no new action. Only its owner or a
   quality manager can add actions to it. See :doc:`corrective_actions`.

**Odoo says "Tag at least one clause before In progress" when I click Start.**
   Tag a clause on the action's :guilabel:`Clauses` tab first. See :doc:`corrective_actions`.

**I do not see the Start or Mark done button on an action.**
   Only the owner of the action or a quality manager can start it or mark it done, so the buttons are shown to them
   only. See :doc:`corrective_actions`.

**Odoo refuses to save an action: "The effectiveness date must be at least N days after the due date."**
   The :guilabel:`Effectiveness gap` setting applies (30 days by default). When you move the due date, move the
   effectiveness date too. See :doc:`corrective_actions`.

**Why is the Verify button missing on my corrective action?**
   It shows only when the action is **Done**, only to its verifier and to quality managers, and never to the action's
   owner, even a quality manager who owns it. Ask the verifier or another quality manager. See
   :doc:`corrective_actions`.

**Verify says "Effectiveness can be judged from <date>".**
   The effectiveness date has not arrived yet. The verdict can be signed from that day on. See
   :doc:`corrective_actions`.

**Who gets the reminder when an action has no verifier?**
   The owner of the nonconformity, unless they also own the action; then the quality managers of the company. See
   :doc:`corrective_actions`.

**The nonconformity shows "Root cause to revisit" and will not close.**
   A corrective action was judged ineffective, or the problem came back. Change the :guilabel:`Root Cause` on the
   :guilabel:`Treatment` tab, then start a new corrective action: the flag clears by itself. See
   :doc:`corrective_actions`.

**Close says "Add a new corrective action and verify that it works".**
   A corrective action of this nonconformity was judged ineffective. It stays on the nonconformity, locked, as the
   record of what was tried. Revise the :guilabel:`Root Cause`, add a new corrective action, start it, carry it out and
   have it verified **Effective**; then the nonconformity can close. An action verified before the ineffective one does
   not count. See :doc:`corrective_actions`.

**A new nonconformity turned my earlier verified action Ineffective.**
   Recurrence detection found the same product, or the same cause category from the same source type, within the
   recurrence window. See :menuselection:`Quality --> Nonconformities --> Recurrences`. A match on the same process alone never does
   this. See :doc:`corrective_actions`.

**Why was no recurrence detected although it is the same problem?**
   Detection runs once, when the nonconformity is accepted, so the product, process or cause category must be set
   before you accept it. A cause-category match also needs the same source type. The earlier nonconformity must be
   detected within the recurrence window and not be cancelled, and a window of 0 switches detection off. See
   :doc:`corrective_actions`.

Audits
======

**Odoo refuses to save an audit: "<user> cannot audit <process>: process owner or auditee."**
   The lead auditor or a co-auditor owns or works in the audited process (:menuselection:`Configuration -->
   Processes`). Choose someone else. Quality managers are not exempt. See :doc:`audits`.

**I cannot choose a colleague as lead auditor or co-auditor.**
   Only users with the :guilabel:`Internal auditor` or :guilabel:`Manager` role are offered, and Odoo refuses anyone
   else. Give them the Internal auditor role first. See :doc:`audits`.

**Approve refuses my audit programme.**
   A programme needs at least one audit that is not cancelled, and every audit planned in a month of the programme's
   year. The message names the audits to move. See :doc:`audits`.

**Start refuses: "Add clauses to the scope" or "The template covers none of the scope clauses".**
   Add clauses on the :guilabel:`Scope and conclusion` tab, or choose a template with questions on those clauses or
   their sub-clauses. See :doc:`audits`.

**I am a co-auditor and cannot start or report the audit.**
   Only the lead auditor starts and reports an audit; a quality manager can do it on their behalf. The buttons are not
   shown to co-auditors, who record checklist results and findings. See :doc:`audits`.

**Report refuses: "Check every line first".**
   Every checklist line needs a result other than :guilabel:`Not checked`. The message names the clauses still open.
   See :doc:`audits`.

**Report or Amend refuses my conclusion.**
   With a major finding, the conclusion must be :guilabel:`Not conforming`; with minor findings and no major one,
   :guilabel:`Conforming with findings`. An amended conclusion follows the same rule. See :doc:`audits`.

**Odoo asks for evidence on a checklist line.**
   :guilabel:`Observation`, :guilabel:`Minor` and :guilabel:`Major` results need evidence, at most 2,000 characters.
   See :doc:`audits`.

**I cannot change the checklist of a reported audit.**
   Reporting signs and locks the checklist, the findings and the conclusion. See :doc:`audits`.

**The findings of my audit have no nonconformity.**
   Nonconformities are created only when a quality manager closes the reported audit, one per minor and major finding.
   Observations never get one. See :doc:`audits`.

**The audit PDF says "DRAFT — not reported".**
   The audit is still in progress. Report it to get the signed version. See :doc:`audits`.

**Why can't my audit start?**
   With the Training & Competence add-on installed, the lead auditor must hold a current internal auditor qualification
   of the level to lead (3 by default) on the start date: *<user> cannot lead this audit: <reason> Record the
   qualification or change the lead auditor.* Grant the qualification, or choose a qualified lead auditor. Otherwise
   Start refuses for the reasons above: no clause in scope, or a template covering none of them. See
   :ref:`audits-qualification` and :doc:`competence`.

**Approve refuses: "Write the programme's rationale (at least 20 characters): why these processes, in these months."**
   Every programme needs its rationale, even when it follows the proposal exactly. See :doc:`audits`.

**Why is Purchasing proposed every 3 months?**
   The proposal starts from the importance of the process and shortens it after major or minor findings, changes and
   nonconformities, never below 3 months. The process's :guilabel:`Basis of the proposal` shows the calculation. See
   :ref:`audits-importance`.

**Odoo says "Only a quality manager can rate the importance of a process."**
   Ask a quality manager; a High or Low importance also needs its reason. See :ref:`audits-importance`.

**The programme will not close.**
   Every audit of the programme must be closed or cancelled first; the message lists those still open. See
   :doc:`audits`.

Documents
=========

**I cannot create a controlled document.**
   Only quality managers create documents. Quality users can write new versions of the documents they can see. See
   :doc:`documents`.

**Odoo says "Finish or delete the open version first" when I click New version.**
   A document has at most one version in **Draft** or **In review**. Submit it and wait for the decision, or delete
   the draft first. See :doc:`documents`.

**My file is refused: "Only PDF, Word, Excel and OpenDocument text files can be controlled".**
   Save the document as PDF, ``.docx``, ``.xlsx`` or ``.odt``. Empty files are refused too. See :doc:`documents`.

**Submit refuses my version.**
   It needs a non-empty file and a change summary, and the document must be tagged with at least one clause on its
   :guilabel:`Clauses` tab. See :doc:`documents`.

**I do not see the Approve button on a version in review.**
   The document type decides who approves: the document owner, a quality manager or top management — never the
   author. The document's :guilabel:`Approved by` field says who. See :doc:`documents`.

**Approve refuses: "<code> is approved by its owner, <owner>."**
   The type's rule is *Document owner* and the owner can approve this version: ask them. Other messages: *Documents of
   type <type> are approved by a quality manager.*, *<code> is approved by top management: <names>.*, *The author
   cannot approve their own version.* See :doc:`documents`.

**Nobody received the Approve to-do of my version.**
   Nobody other than the author can approve it under the type's rule, and the version's chatter says so. Give the
   document an owner who did not write it, give a quality manager the approval, or — for the quality policy — name
   the top management in the Quality settings. See :doc:`documents`.

**Approving the quality policy asks me to confirm four points.**
   ISO 9001 clause 5.2.1: the policy fits the purpose and context, frames the objectives, commits to requirements and
   commits to continual improvement. Tick the four boxes; Odoo names the one missing. See
   :ref:`documents-quality-policy`.

**Odoo says "<company> already has a quality policy in force (<version>); revise it instead."**
   Each company has one quality policy in force. Write a new version of the existing policy document. See
   :ref:`documents-quality-policy`.

**Submit refuses: "Give the edition of this external document (for example 2015 or Rev C)."**
   A version of an external document must say which edition of the issuer it holds. See :doc:`documents`.

**Odoo says "Portal and public groups cannot be an audience: name portal readers one by one."**
   Portal readers are added one by one under :guilabel:`Portal readers`, never through a group. See
   :ref:`documents-portal-readers`.

**Why was a record not deleted when its retention period ended?**
   Nothing is ever deleted automatically. A record past its *Keep until* date shows a banner and appears under
   :guilabel:`Past retention`; disposal is a manual decision taken outside the system. See
   :ref:`documents-retention`.

**An approved version became Obsolete without ever being in force.**
   A newer version of the same document came into force before its date, so the older one was superseded; its chatter
   says *Superseded by … before it came into force*. See :doc:`documents`.

**I approved a version but it is not in force.**
   An approved version comes into force on its :guilabel:`Effective from` date, at the next daily run. A quality
   manager can click :guilabel:`Make effective` to bring it into force today. See :doc:`documents`.

**My version disappeared after I submitted it.**
   A quality user sees their own versions only while they are draft or rejected. It reappears when it comes into
   force, or when it is rejected. See :doc:`documents`.

**Odoo says "Open the file first" when I click Read and understood.**
   Click :guilabel:`Open the file` in the message or on the line first: the line turns *Opened*, then
   :guilabel:`Read and understood` is available. Odoo keeps the first opening, so you do not need to open it again after
   logging out. See :doc:`documents`.

**Can a manager acknowledge a document for someone who has no computer access?**
   No. Only the reader can acknowledge, for themselves. See :doc:`documents`.

**An audience member was not asked to read the document.**
   Readers need at least the Quality :guilabel:`User` role; members without it are skipped, and the version's chatter
   names them. Add the role to their user: they are asked at the next daily run. See :doc:`roles`.

**Odoo says "The file of … no longer matches the hash recorded at upload".**
   The stored file was changed outside the application after it was uploaded. It can no longer be approved, opened or
   printed. Contact your administrator, and create a new version with the right file. See :doc:`documents`.

**How do I answer the periodic review to-do?**
   Either bring a new version into force, or, when the document did not need to change, click :guilabel:`Reviewed, no
   change`. Both move the next review date on and close the to-do. See :doc:`documents`.

**Why is my Word document printed as a single cover page?**
   The Odoo server has no LibreOffice converter. The cover page names the file and its SHA-1 fingerprint. Upload a PDF
   to print the content itself. See :doc:`documents`.

**The master list says "none in force" for a document.**
   No version of that document was in force on the chosen date: it was not yet effective, or it was withdrawn. See
   :doc:`documents`.

Management reviews
==================

**Hold refuses: "Discuss or note every input first".**
   Each input needs the :guilabel:`Discussed` switch on or some notes. The message lists the inputs still open. See
   :doc:`management_reviews`.

**Approve refuses although the meeting was held.**
   Approval needs a conclusion, the :guilabel:`Discussed` switch on for every input (notes are not enough), and an
   owner and a due date on every decision. Only the chair can approve. See :doc:`management_reviews`.

**I cannot choose a person as chair of a review.**
   The chair must be a quality manager of the review's company; only they are offered. See :doc:`management_reviews`.

**I cannot change the decisions of an approved review.**
   After approval only the :guilabel:`Status` of a decision can change. A quality manager can amend the conclusion
   with :guilabel:`Amend`. See :doc:`management_reviews`.

**Printing the minutes says "Hold the meeting first".**
   A draft review has no minutes, whether you use the button or the :guilabel:`Print` menu. See
   :doc:`management_reviews`.

**Odoo says "The figures are frozen once the meeting is held".**
   :guilabel:`Recompute inputs` works only on a draft review. See :doc:`management_reviews`.

**Create action refuses: "Hold the meeting before creating actions from its decisions".**
   Hold the review first. The decision also needs an owner and a due date, and only quality managers create actions
   from decisions. See :doc:`management_reviews`.

**An input reads "component not installed — record the discussion in the notes".**
   The figures of that input come from a part of the app that is not installed. Discuss it from your notes. See
   :doc:`management_reviews`.

**An input reads "No risk register entries for the period".**
   The register had nothing in the review period. The sentence replaces a row of zeros. See :doc:`management_reviews`.

**The Next management review tile is missing.**
   It needs at least one approved review, and a :guilabel:`Review interval` above 0. See :doc:`management_reviews`.

**I do not get the management review reminder.**
   It goes to quality managers only, within the reminder window, and not while any review of the company is draft or
   held. See :doc:`management_reviews`.

Audit pack
==========

**My audit pack stays "Queued".**
   Another pack of the same company is generating. Packs are built one at a time per company, in the order they were
   requested; the next one starts at the next run of the scheduled action, every 10 minutes. See :doc:`audit_pack`.

**Odoo says "The period exceeds 24 months: split the pack."**
   The :guilabel:`Longest period` setting applies (24 months by default). Request two packs. See :doc:`audit_pack`.

**Odoo says "A pack cannot cover the future".**
   The period must end today at the latest. See :doc:`audit_pack`.

**My pack failed with "timeout".**
   It ran longer than the :guilabel:`Time cap` (600 seconds by default). Raise the cap or shorten the period, then
   request a new pack: a failed pack is never restarted. See :doc:`audit_pack`.

**My pack failed with "interrupted".**
   The server restarted while the pack was generating. Request a new pack. See :doc:`audit_pack`.

**Why can't I download the files of a failed pack?**
   A failed pack has no ZIP. Its rows only show which files were built before the failure. See :doc:`audit_pack`.

**sha256sum on the ZIP does not give the bundle hash.**
   That is expected: the bundle hash is computed from the SHA-256 values of the files, not from the bytes of the ZIP.
   The audit pack page gives the command that recomputes it from ``README.txt``. See :doc:`audit_pack`.

**Preview or Download of a pack file says it "no longer matches its SHA-256".**
   The file inside the stored ZIP was changed outside Odoo, so Odoo refuses to serve it. Inform your system
   administrator. See :doc:`audit_pack`.

**I cannot delete an audit pack.**
   Done packs are evidence and are never deleted; queued and generating packs cannot be deleted either. Only a quality
   manager can delete a failed or cancelled pack. See :doc:`audit_pack`.

**I cannot cancel a pack.**
   Only a queued pack can be cancelled, by the person who requested it or by a quality manager. A generating pack runs
   until it is done or fails. See :doc:`audit_pack`.

Context, risks and objectives
=============================

**Odoo says "Use Mark reviewed or Retire: the review and the state are not written directly."**
   The review dates of a context issue move only with :guilabel:`Mark reviewed`, which needs a note of at least ten
   characters. Only the owner or a quality manager can use it. See :doc:`context`.

**Approve refuses my scope: "A scope approved today is in force; approve its revision from tomorrow."**
   Two versions cannot come into force on the same day. Approve the revision tomorrow. See :doc:`context`.

**My scope shows "Clause applicability changed since this scope was approved".**
   A clause was declared not applicable, or made applicable again, since the scope was signed. Revise the scope and
   approve the revision. See :doc:`context`.

**Open refuses my risk: "Add at least one treatment action." or "Write a treatment note of at least 10 characters."**
   Reduce, avoid, transfer and pursue need a treatment action; accept and decline need a note. See :doc:`risks`.

**I picked Accept in the Treatment field and Odoo put it back.**
   Acceptance is not chosen in the field: the :guilabel:`Accept` button records who accepted the risk and why. The
   window "Accepting a risk" says so and keeps your other changes; if you may accept the risk it offers
   :guilabel:`Accept now…`, which saves the form and opens the Accept dialog. A high or critical risk is accepted by a
   quality manager, with a note and their signature; anyone else asks one, or chooses Reduce, Avoid or Transfer. The
   same kind of window guides you when a value only a button sets (Override significance, Activate, Withdraw, Sign,
   Close, Void) reaches a save. See :doc:`risks`.

**A risk, aspect, hazard or other register record shows "Only the owner (…) or a quality manager can work on this …".**
   Its buttons belong to the named person and to quality managers; ask one of them. Internal auditors see "Auditors have
   read-only access." instead.

**Odoo says "Re-assess the risk to change its score."**
   Once a risk is open, its score changes only through :guilabel:`Re-assess`, which keeps the history. See
   :doc:`risks`.

**Close refuses: "Finish or cancel the treatment actions first."**
   A treatment action is still in draft or in progress. See :doc:`risks`.

**Activate refuses: "Complete these items before activating the objective: …"**
   The plan texts, a clause and, with a quality policy in force, how the objective serves it are missing. See
   :doc:`objectives`.

**Odoo says "Only a quality manager changes the target or the period of an active objective."**
   The owner records measurements; a quality manager changes the target, and the change is shown on the objective.
   See :doc:`objectives`.

**Odoo says "The objective already has a measurement on this date; correct that one."**
   There is one measurement per date. Open it and correct its value. See :doc:`objectives`.

Satisfaction and calibration
============================

**Odoo says "The period has not ended yet: record the result once the period is over."**
   A satisfaction result is recorded after its period. See :doc:`satisfaction`.

**Why does my satisfaction record say "Action expected"?**
   It was below its target or dropped by at least the deterioration threshold since the previous result. Raise an
   improvement action, or have a quality manager record why none is needed. See :doc:`satisfaction`.

**Why does an instrument say DO NOT USE?**
   It is overdue, out of tolerance, never calibrated, out of service or retired. See :doc:`calibration`.

**Confirm refuses my calibration.**
   An external calibration needs its certificate file (*Attach the calibration certificate.*), an in-house one its notes;
   the traceability fields must be filled in, and a broken protection restored first (*Restore the protection before
   confirming, or put the equipment out of service.*). See :doc:`calibration`.

**The nonconformity of an out-of-tolerance calibration will not close.**
   Record the impact assessment on the calibration: *Record the impact assessment of <calibration> (measurements from
   <date> to <date>).* See :doc:`calibration`.

Training and competence
=======================

**Is the acknowledgement matrix a training record?**
   No. The acknowledgement matrix shows who confirmed they read and understood each controlled document, and when: it
   is evidence of awareness (ISO 9001 7.3). Competence (7.2) is recorded by the Training & Competence add-on, as
   competence records, trainings and the competence matrix. An acknowledgement never creates or extends a competence
   record. See :doc:`competence`.

**Where do I install Training & Competence?**
   It is a separate free module, installed separately from **Apps**; it needs Employees. Record the auditor
   qualifications first: from then on, an audit whose lead auditor is not qualified cannot start. See
   :doc:`competence`.

**Mark done refuses my training.**
   Every attendee needs a result (*Record a result for every attendee.*), and an external course a certificate for
   every attendee who passed. See :doc:`competence`.

**Odoo says "A training record is granted by marking its training done."**
   Records of source *Training* come only from a training marked done. Record an assessment or prior experience
   instead, or mark the training done. See :doc:`competence`.

**Odoo says "Nobody evaluates their own training."**
   The employee's manager or a quality manager evaluates it; never the attendee or the trainer. See
   :doc:`competence`.

**A "not effective" verdict removed a competence.**
   That is intended: a training that did not work grants nothing, so its records are revoked and the gap shows again.
   See :doc:`competence`.

Suppliers
=========

**Why do buyers get a warning?**
   The :guilabel:`Purchase confirmation control` is *Warn* (the default) and the supplier is unapproved or blocked:
   *<supplier> is not on the approved supplier list.* or *<supplier> is blocked by <decision> (<date>, <signer>).* The
   buyer can confirm anyway with a reason. Right after installing the add-on every supplier is unapproved: set the
   control to *Off* while you build the approved supplier list. See :doc:`suppliers`.

**Confirmation is refused for a supplier.**
   The control is *Block*: sign a decision for the supplier, or confirm from another supplier. See :doc:`suppliers`.

**Accept refuses a supplier nonconformity: "Name the supplier of this nonconformity."**
   Choose the :guilabel:`Supplier` first. When the nonconformity was raised from a purchase order or a receipt, the
   supplier follows it and cannot be changed. See :doc:`suppliers`.

**A supplier shows "Not rated".**
   It had no receipt in the period, or Inventory is not installed, so the receipt measures are missing. See
   :doc:`suppliers`.

**Sign refuses: "This decision departs from <evaluation> (proposed <status>) …"**
   The full message asks you to cite the evaluation and explain why in at least 30 characters. A decision that differs from the latest evaluation's proposal cites it and says why. See :doc:`suppliers`.

**Odoo says "Record the supplier's response before marking this SCAR done."**
   Record the supplier's answer on the :guilabel:`Supplier` tab of the SCAR. See :doc:`suppliers`.

**A requirement shows "Revision not communicated".**
   A newer version of one of its documents is in force. Supersede the requirement and communicate the new one. See
   :doc:`suppliers`.

Environment, health and safety
==============================

**Why can't I see Environment (or the EHS menu, or Safety reports)?**
   The environment, health and safety registers are off until a quality manager ticks :guilabel:`ISO 14001
   environmental registers` or :guilabel:`ISO 45001 health & safety registers` in :menuselection:`Settings -->
   Quality` and saves. The :guilabel:`Environment` section needs the ISO 14001 box, :guilabel:`Health & Safety` the
   ISO 45001 box; :guilabel:`Shared` and Safety reports show with either. The **Quality** menus need a Quality role;
   Safety reports does not. See :doc:`ehs_setup`.

**I switched the ISO 45001 registers off. Are my hazards gone?**
   No. Switching a box off hides the registers; nothing is deleted. Tick it again and everything is back.

**Odoo says "Turn off the ISO 14001 environmental registers first."**
   You removed ISO 14001 from the enabled standards while its registers are on. Untick the box first, or in the same
   save. See :doc:`ehs_setup`.

**Who can read injury details?**
   Quality managers only. Quality users and internal auditors see the person's name and role on an incident, never the
   body part, nature, treatment or days lost; the incident log PDF and the nonconformity raised from an incident
   contain none of them. Do not write health details in the nonconformity or in the messages. See :doc:`incidents`.

**Is a confidential report anonymous?**
   No. Only quality managers see who sent a confidential worker hazard report; everyone else reads *Confidential
   reporter*. The server's technical logs and a database administrator can still identify the reporter. There is no
   anonymous or portal reporting. See :doc:`safety_reports`.

**"Report" refuses my incident: "A report gives what happened, when, where and who was involved; …"**
   A report without a Quality role gives only the event itself; the owner, clauses, reportability and investigation are
   set by the quality team after triage. See :doc:`safety_reports`.

**I am an internal auditor and I do not see "Report an incident".**
   Internal auditors read the incident log and record nothing in it, so the entry is not shown to them. Ask a
   colleague or a quality manager to report the incident, or report the hazard. See :doc:`incidents`.

**Close refuses my incident with a list: "Before closing INC/…: …"**
   Each line is something its type still needs: the injured person's details, the reportability decision, the date
   the authority was notified, the nonconformity with its root cause (or, for a near miss, an investigation summary),
   an investigator, the potential severity or the release medium, and an outcome of at least 20 characters. Only a
   quality manager closes an incident. See :doc:`incidents`.

**My nonconformity from a legal evaluation will not close: "Record a compliant re-evaluation of LEG-…".**
   It closes once a later evaluation of the same obligation is confirmed *Compliant*. See :doc:`legal_requirements`.

**My nonconformity from a reading will not close: "The latest reading of MON-… still exceeds the legal limit".**
   Record the next reading, within the limit, then close it. See :doc:`monitoring`.

**Confirm asks me to "Justify the compliant result against the … legal-limit exceedances listed".**
   Readings beyond the obligation's legal limit were recorded in the evaluation window. Explain in
   :guilabel:`Justification` why the obligation is still complied with, or choose another result. See
   :doc:`legal_requirements`.

**Done refuses my drill: "Record the lessons learned and at least one follow-up action or nonconformity."**
   A partially effective drill needs lessons learned and an improvement action or a nonconformity; a drill that was
   not effective needs a nonconformity. Add them with the buttons on the planned drill, then click :guilabel:`Done`. An
   effective drill cannot be slower than the situation's target response time. See :doc:`emergency_preparedness`.

**Open refuses my aspect: "A significant aspect needs a control: …".**
   Give it an operational control of at least 20 characters, a document, a control action or an objective. See
   :doc:`environmental_aspects`.

**Open refuses my hazard: "A high or critical hazard needs at least one further control."**
   Click :guilabel:`Add further control` first. A critical hazard controlled by protective equipment only also needs a
   PPE justification. See :doc:`hazards`.

**Odoo says "Re-assess the hazard to change its score." (or the aspect).**
   Once open, the score changes only through :guilabel:`Re-assess`, which keeps the history.

**My reading is wrong. Can I correct it?**
   No: void it with a reason and enter the right value as a new reading. The person who recorded it may void it the
   same day, unless it is beyond the legal limit; otherwise a quality manager does. See :doc:`monitoring`.

**Where do I print the legal register (or the hazard register, the incident log …)?**
   In the register's section of :menuselection:`Quality --> EHS`, right after the register, for example
   :menuselection:`Quality --> EHS --> Shared --> Print legal register`; the list's :guilabel:`Actions` menu offers it
   too. The same registers are files 17 to 23 of the audit pack. See :doc:`audit_pack`.

**The worker hazard report tile is red.**
   A report is past its triage day (5 days after submission by default). Close it with an outcome the reporter reads.
   See :doc:`worker_consultation`.

Settings and access
===================

**A quality user does not see the Audit pack menu.**
   Audit packs are for internal auditors and quality managers only. See :doc:`roles`.

**I am a quality manager but cannot open the Quality settings.**
   The Settings app opens only for users with the *Administration: Settings* right. Ask your administrator to change
   the settings, or to give you that right. See :doc:`configuration`.

**A person does not see the Quality app at all.**
   They have no Quality role. Set one in :menuselection:`Settings --> Users & Companies --> Users`, on the
   :guilabel:`Access Rights` tab. See :doc:`roles`.

**I do not see the Configuration menu.**
   :menuselection:`Quality --> Configuration` (standards, clause applicability, processes, audit templates, document
   types, review inputs, record retention, competences, assessment criteria) is for quality managers only. See
   :doc:`roles`.

**I work for two companies and some records are missing.**
   You see the records of the companies selected in the company switcher. Select the other company too. See
   :doc:`roles`.

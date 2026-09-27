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

Operations
==========

**The Raise nonconformity button is missing on a receipt or an order.**
   The user needs a Quality role, and the source module for that app must be installed. Each source module installs
   itself when both the Quality app and the app it connects to are installed. See :doc:`sources`.

**I cannot change the Source Type of a nonconformity raised from a receipt.**
   A nonconformity raised from a record keeps the source type that record gives it. To record the problem under
   another source type, create the nonconformity from :menuselection:`Quality --> Nonconformities`. See
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
   recurrence window. See :menuselection:`Quality --> Recurrences`. A match on the same process alone never does
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
   Only quality managers approve, and never the author of the version. Ask another quality manager. See
   :doc:`documents`.

**Nobody received the Approve to-do of my version.**
   The to-do goes to quality managers other than the author. When the author is the company's only quality manager,
   nobody can approve: the version's chatter says so. Give another person the Manager role. See
   :doc:`documents`.

**An approved version became Obsolete without ever being in force.**
   A newer version of the same document came into force before its date, so the older one was superseded; its chatter
   says *Superseded by … before it came into force*. See :doc:`documents`.

**I approved a version but it is not in force.**
   An approved version comes into force on its :guilabel:`Effective from` date, at the next daily run. A quality
   manager can click :guilabel:`Make effective` to bring it into force today. See :doc:`documents`.

**My version disappeared after I submitted it.**
   A quality user sees their own versions only while they are draft or rejected. It reappears when it comes into
   force, or when it is rejected. See :doc:`documents`.

**Odoo says "Open the document first" when I click Read and understood.**
   Click :guilabel:`Open the file` in the same session first. After logging out and back in, open it again. See
   :doc:`documents`.

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
   :menuselection:`Quality --> Configuration` (standards, processes, audit templates, document types) is for quality
   managers only. See :doc:`roles`.

**I work for two companies and some records are missing.**
   You see the records of the companies selected in the company switcher. Select the other company too. See
   :doc:`roles`.

=========
Dashboard
=========

The Quality dashboard is the quality manager's morning screen: how many nonconformities are open and how old they
are, what is overdue, and how they split by severity and by source. Every tile opens the records it counts.

Go to :menuselection:`Quality --> Dashboard`.

.. image:: ../_images/dashboard.png
   :alt: The Quality dashboard with the open-by-age, overdue, severity, source and amended-records tiles.

Every figure is counted with your own access rights: a quality user who only sees the nonconformities they own,
detected or follow gets figures for those records only. A quality manager or internal auditor sees the whole
company. See :doc:`roles`.

The tiles
=========

The free core shows five tiles, in this order:

.. list-table::
   :header-rows: 1
   :widths: 25 45 30

   * - Tile
     - Counts
     - Shown as
   * - :guilabel:`Open nonconformities by age`
     - New and open nonconformities, split by the number of days since their detection date. With the default age
       buckets: *0-30*, *31-60*, *61-90* and *>90* days.
     - A ring with the total in the middle and, next to it, each bucket with its count and share.
   * - :guilabel:`Overdue nonconformities`
     - New and open nonconformities whose due date has passed.
     - A number and a history line of the last eight months, captioned *Due dates missed per month*.
   * - :guilabel:`Nonconformities by severity, open and closed`
     - New, open and closed nonconformities, split into :guilabel:`Minor`, :guilabel:`Major` and
       :guilabel:`Critical`.
     - A ring with the total and each severity with its count and share.
   * - :guilabel:`Nonconformities by source, open and closed`
     - New, open and closed nonconformities, split by source type (:guilabel:`Audit`, :guilabel:`Complaint`,
       :guilabel:`Inspection`, :guilabel:`Supplier`, :guilabel:`Internal`, :guilabel:`Health, safety and
       environment`).
     - One bar per source type, with its count and share.
   * - :guilabel:`Amended nonconformities`
     - Nonconformities that were amended at least once after closing, whatever their state.
     - A number and a history line of the last eight months, captioned *Amendments per month*.

Cancelled nonconformities are never counted. A source type or severity with no nonconformity does not appear on its
tile.

.. note::
   Age is counted from the :guilabel:`Detected On` date, not from the date the record was entered.

Colours
-------

Each tile has its own tint so that the eye finds it quickly: red for :guilabel:`Overdue nonconformities`, amber for
:guilabel:`Nonconformities by severity, open and closed`, grey for :guilabel:`Amended nonconformities`, and blue for the age and
source tiles. A tile that counts things needing attention is tinted red or amber only while its number is above zero;
at zero it turns green, so a green card always means nothing waits for you.

In the rings and bars, each part has its own colour. The age buckets go from green (the youngest) through amber and
orange to red (the oldest), so a ring that turns red means old open nonconformities.

History and trend
-----------------

The :guilabel:`Overdue nonconformities` and :guilabel:`Amended nonconformities` tiles show a small grey line of the last
eight months, the current month last. A caption under the line says what it counts, because it is a history, not the
number above it:

- on :guilabel:`Overdue nonconformities`, *Due dates missed per month*: each month counts the nonconformities that fell
  due in that month and were not closed by their due date;
- on :guilabel:`Amended nonconformities`, *Amendments per month*: each month counts the amended values recorded in that
  month (an amendment that changes two fields counts twice).

The other tiles with a history, such as :guilabel:`Recurrences (90 days)`, are captioned the same way. A small badge
under a number, such as *1 overdue* or *3 > 90 days*, always counts part of that number; no badge compares the number
with last month.

Open the records behind a tile
==============================

Click anywhere on a tile. The nonconformity register opens, titled with the name of the tile, on exactly the records
the tile counts. The register's usual :guilabel:`Open` filter is not applied, so nothing is hidden or added.

For a tile split into parts, the click opens all the records of the tile, not only one part. To go further, group the
list, for example by :guilabel:`Severity` or :guilabel:`Source`.

.. tip::
   :guilabel:`Overdue nonconformities` opens the late ones directly: a good list to review in the weekly quality
   meeting.

My records
==========

Click :guilabel:`My records` at the top right to see only the nonconformities you own. The button turns solid while it
is on, and every tile, including the history lines, is recounted. Click it again to see everything you are allowed to
see.

.. note::
   :guilabel:`My records` counts the nonconformities you **own**. The :guilabel:`My NCs` filter of the register is
   wider: it also includes those you detected.

Change the age buckets
======================

The age buckets are set in :menuselection:`Settings --> Quality`, under :guilabel:`Dashboard age buckets`: a list of
day counts separated by commas, each the upper limit of one bucket. The default ``30,60,90`` gives *0-30*, *31-60*,
*61-90* and *>90* days. A food plant might prefer ``7,14,30``; an engineering company ``30,90,180``. See
:ref:`config-age-buckets`.

Tiles added by QMS Advanced
===========================

With **QMS Advanced** installed, the dashboard shows more tiles after the five above:

- :guilabel:`Overdue corrective actions`, :guilabel:`Actions awaiting a verdict` and :guilabel:`Recurrences (90 days)`
  — see :doc:`corrective_actions`;
- :guilabel:`Audit programme completion (%)` and :guilabel:`Open audit findings` — see :doc:`audits`;
- :guilabel:`Documents overdue for review` and :guilabel:`Acknowledgements pending` — see :doc:`documents`;
- :guilabel:`Next management review` — see :doc:`management_reviews`;
- :guilabel:`Context reviews due` — see :doc:`context`;
- :guilabel:`High and critical risks` — see :doc:`risks`;
- :guilabel:`Objectives at risk` — see :doc:`objectives`;
- :guilabel:`Satisfaction records awaiting action` — see :doc:`satisfaction`;
- :guilabel:`Calibration due` — see :doc:`calibration`.

While the environment, health and safety registers are switched on (see :doc:`ehs_setup`), nine more tiles follow,
each shown only with the registers of its standard:

.. list-table::
   :header-rows: 1
   :widths: 28 52 20

   * - Tile
     - Counts
     - Page
   * - :guilabel:`Legal compliance`
     - Active obligations whose evaluation is overdue, whose permit is expiring or expired, or whose latest result is
       not compliant; red with the badge *N permit(s) expired* or *N evaluation(s) overdue* when there are some.
     - :doc:`legal_requirements`
   * - :guilabel:`Emergency situations to act on`
     - Active emergency situations whose drill is due soon or overdue, whose plan is not in force or whose plan
       review is late; the badge joins *N overdue*, *N plan(s) not in force* and *N review(s) late*.
     - :doc:`emergency_preparedness`
   * - :guilabel:`Monitoring readings overdue`
     - Active indicators whose reading is overdue.
     - :doc:`monitoring`
   * - :guilabel:`Legal limits exceeded (30 days)`
     - Readings beyond a legal limit recorded within the look-back days (30 by default); red while there are some.
     - :doc:`monitoring`
   * - :guilabel:`Significant aspects` (ISO 14001)
     - Open significant aspects; red when one lacks a control or is overdue for review.
     - :doc:`environmental_aspects`
   * - :guilabel:`High and critical hazards` (ISO 45001)
     - Open high and critical hazards; red when one needs a further control, is overdue for review, or is critical
       with protective equipment only and no justification.
     - :doc:`hazards`
   * - :guilabel:`Incidents to triage`
     - Reported incidents not yet triaged; red when one waits longer than the triage days.
     - :doc:`incidents`
   * - :guilabel:`Worker hazard reports` (ISO 45001)
     - Open worker hazard reports; red with the badge *N overdue* when one is past its triage day.
     - :doc:`worker_consultation`
   * - :guilabel:`Authority reports due`
     - Open reportable incidents not yet notified to the authority; red when one is overdue.
     - :doc:`incidents`

The :guilabel:`Calibration due` tile counts the instruments due soon, overdue, never calibrated or out of tolerance;
its badge joins *N overdue* and *N not usable* (never calibrated or out of tolerance). For the legal, drill and monitoring tiles, a quality user counts the records they own or are responsible for;
internal auditors and quality managers count all. :guilabel:`My records` narrows the tiles to the records you own,
except :guilabel:`Incidents to triage`, which always counts every report waiting, and :guilabel:`Worker hazard
reports`, which then counts the reports you have in review.

The add-ons add their own tiles: :guilabel:`Competence gaps`, :guilabel:`Qualifications expiring` and
:guilabel:`Training evaluations due` with Training & Competence (see :doc:`competence`), and :guilabel:`Suppliers
needing attention` with the supplier evaluation (see :doc:`suppliers`).

.. seealso::
   - :doc:`nonconformities`
   - :doc:`configuration`

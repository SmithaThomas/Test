The system has provision of generating separate reports for stopped alerts based
on the contact method. For phone and SMS contacts, Utility CSRs need a provision
to add alert stop such that they can put stop on any number when required. In
the following section, we will discuss the details of the proposed
implementation and the final implementation in alerts system.

Proposed Implementation
-----------------------

The *Stopped Alerts* reports for both phone and SMS will have an *Add Alert
Stop* button. A sample of this implementation is as shown in the image,

![stoppedsms.PNG](media/038b0445aaafb4714779eae016083187.png)

Image : Add Alert Stop Button

This button will display a lookup box where a contact number is entered, such
that the corresponding profiles are displayed.

![lookup.png](media/46ca7aa79b75e94af77d9dacaeb6eb7a.png)

Image : Lookup

![alert stop.png](media/e8ae5cd9aaf482d01d61b84fd0a5e7a5.png)

Image : Alert Stop

The different profiles associated with the contact number will be listed as
shown the image. The Utility CSR can select a particular profile or all the
profiles listed and disable them. If SMS and/or phone alerts for the number has
to be stopped irrespective of its profiles, the checkboxes should be selected.
The *Add Alert Stop* button will create a stop on all the alerts associated to
the contact method.

Implementation in Alerts Engine
-------------------------------

An *Add Alert Stop* button is added along with the *Stopped Alerts* report.

![stoppedsms imple.PNG](media/d008882fe13e5471b877e48dbf89683e.png)

Image : Add Alert Stop Button

*Add Alert Stop* button displays a lookup pop-up, where users can search for a
contact. The choice for the type of contact is available, based on which the
related profiles are listed.

![lookup imple.png](media/c326f567063f2bef545e27a60f82ff24.png)

Image : Lookup Pop-up

![alert_stop1.png](media/a6af43ccd6d1ce769aecb1501213f7f1.png)

Image : Alert Stop

This screen displays the Account Ids related to the contact number, type of
contact, Is Stopped (if the contact is stopped or not) and checkboxes to disable
the profiles. Options to add alert stop to a profile and/or disable are
available. *Add Alert Stop* button will add a stop to all the entries and
individual checkboxes have to be selected to disable the profiles.

The codebase used for this functionality are

Report page template file:
<https://github.com/exceleron/PAMS-WWW/blob/alerts/templates/en-us/reports/stopped_alerts.tt>

Lookup:
<https://github.com/exceleron/PAMS-WWW/blob/alerts/templates/en-us/reports/get_destination.tt>

JavaScript file:
<https://github.com/exceleron/PAMS-WWW/blob/alerts/root/static/js/pams/pams.reports.js>

Controller file:
<https://github.com/exceleron/PAMS-WWW/blob/alerts/lib/PAMS/WWW/Controller/Reports/Other.pm>

In controller, the three subroutines used for Add Alert Stop are
get_destination, add_alert_stop and disable_contacts.

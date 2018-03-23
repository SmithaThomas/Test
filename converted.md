| <img src="media/image1.png" width="323" height="64" /> |
|--------------------------------------------------------|
| User Management                                        |
|                                                        |
|                                                        |
|                                                        |
|                                                        |

|     |
|-----|

Document Revision 1.0

2016/11/14

[\_Toc460518945](#_Toc460518945)

[\_Toc460518945](#_Toc460518945)

Introduction
============

There are three categories of users in the application, Admin, Utility
users and Account. ESI and API roles are aligned to Admin category. Each
user is assigned a particular role. Based on the role assigned, users’
permissions vary and they are allowed to access and perform different
actions in the application.

<span id="_1fob9te" class="anchor"><span id="_Toc490149005" class="anchor"></span></span>Role Management (URL: /manage/roles)
-----------------------------------------------------------------------------------------------------------------------------

Role management is handled in the *Manage Roles* tab.

Each category of the user will have different roles to perform actions

Admin:

ESI - This is a model role for Exceleron users

> API.Alerts - This is a model role for APIs related to Alerts
>
> API.IVR - This is a model role for APIs related to IVR
>
> API.InboundSMS - This is a model role for APIs related to Inbound SMS

Utility:

> Util.CSR - This is a model role for a Utility user, which represents a
> customer service representative
>
> Util.Manager - This is a model role for a Utility user, which
> represents a Manager

Account:

Account - This is a model role for an Account holder

<img src="media/image2.png" width="541" height="362" />

Image 1: Manage Roles

Manage screen allows the ESI, Utilities to create a new role and
modifying it. None of the default roles can be deleted and ESI role
cannot be disabled. Permissions option displays the permissions allowed
for a role.

**Role Description**

The default roles and its settings are mentioned in the below table:

| **ID** | **Name**       | **Type** | **Description**                                                           | **UtilityId** |
|--------|----------------|----------|---------------------------------------------------------------------------|---------------|
| 1      | ESI            | Admin    | Allowed access to all URLs and APIs                                       | 0             |
| 2      | Util.Manager   | Utility  | Allowed access to URLs specific for Manager and Account                   | 0             |
| 3      | Util.CSR       | Utility  | Allowed access to URLs specific for Account and CreateProfileAlerts setup | 0             |
| 4      | Account        | Account  | Allowed access to Account specific URLs                                   | 0             |
| 5      | API.Alerts     | API      | Allowed access to all APIs except UpdateCallAlerts                        | 0             |
| 6      | API.IVR        | API      | Allowed access to GetCallAlerts, UpdateCallAlerts                         | 0             |
| 7      | API.InboundSMS | API      | Allowed access to InboundSMS                                              | 0             |

Table 1: Default Roles

Creating a new role in the UI happens as follows by selecting the
*Create New Role* button.

<img src="media/image3.png" width="345" height="198" />

Image 2: Create Role

While creating a new role, the *Name*, *Type* and *Description* are
furnished. On selecting either Utility or Account as the *Type*,
*Utility* field appears and the respective Utility name has to be
selected.

Editing a role can be done by selecting the *Edit* button. Editing
screen is shown below in the image:

<img src="media/image4.png" width="370" height="212" />

Image 3: Edit Role

Default Utility roles have an additional option called Auto Assign. This
option decides if a new feature has to be automatically assigned to a
user or not.

<img src="media/image5.png" width="375" height="199" />

Image 4: Auto Assign

-   If *Auto Assign* is Yes, then features will be assigned
    automatically

-   If *Auto Assign* is No, then features will not be
    assigned automatically. It will still be available in Features
    Notification screen but un-checked.

-   If *Auto Assign* is Suggest, then Utility users are allowed to
    choose/save a feature in Features Notification screen. When feature
    will be checked if the *Auto Assign* is set to Suggest.

> Feature notification screen is where a user can select a feature from
> the list.
>
> <img src="media/image6.png" width="620" height="247" />

Image 5: Features Notification

Deleting a role can be done using the *Delete* button. On selecting the
button, a confirmation message is displayed. Default roles cannot be
deleted, the delete option is greyed out.

<img src="media/image7.png" width="431" height="139" />

Image 6: Delete Role

*Disable* button is used to disable a role if required. The *Disable*
button will be greyed out for ESI role.

<img src="media/image8.png" width="484" height="152" />

Image 7: Disable Role

*Permissions* button is used to display the permissions allowed for a
role. It has *Available Permissions* and *Assigned Permissions* fields,
where permissions/URL can be assigned to the role.

<img src="media/image9.png" width="624" height="463" />

Image 8: Permissions

All the available URLs and permission will be listed in the *Available
Permissions* field and they can be moved to the *Assigned Permissions*
field. *Update Permissions* button would save the changes.

<span id="_30j0zll" class="anchor"><span id="_Toc490149006" class="anchor"></span></span>Admin Users (URL: /admin/users)
------------------------------------------------------------------------------------------------------------------------

Exceleron users are the admin users. This manage screen and the other
related actions are applicable for both ESI and API users. The tabs
accessible for admin users as shown in the image:

<img src="media/image10.png" width="523" height="186" />

Image 9: Admin Users login

*Create User* button allows an admin to create a new user.
*Email/UserName*, *User Type*, *Base Role* and *Password* are set to
create a new user. User role field allows the user to inherit the
additional roles. *Email/UserName*, *Choose Password* and *Confirm
Password* fields are mandatory fields. If an admin user has to be
created, Admin should be selected for *User Type* with ESI
auto-populated for the *Base Role*. An admin can have API roles as
additional roles.

<img src="media/image11.png" width="387" height="269" />

Image 10: Create Admin User

If an API user has to be created, API should be selected for *User Type*
with API.IVR auto-populated for the *Base Role*. API roles cannot have
ESI as an additional role.

<img src="media/image12.png" width="459" height="350" />

Image 11: Create API User

*Edit* button is used to modify the settings for admin users.

<img src="media/image13.png" width="404" height="237" />

Image 12: Edit Admin User

On selecting the checkbox for *Change Password*, *Choose Password* and
*Confirm Password* fields will be displayed.

<img src="media/image14.png" width="270" height="69" />

Image 13: Password Fields

*Delete* button allows the delete action, where created user information
can be removed.

<img src="media/image15.png" width="450" height="137" />

Image 14: Delete Admin User

<span id="_2et92p0" class="anchor"><span id="_Toc490149007" class="anchor"></span></span>Utility Users (URL: /utility/users)
----------------------------------------------------------------------------------------------------------------------------

Utility Managers and Utility CSRs are the Utility users. The Utility
users’ manage screen is shown in the image below:

<img src="media/image16.png" width="624" height="196" />

**Image 15: Utility Users login**

The manage screen displays the *Utility*, *Id*, user’s *Email* address,
and *Role*. *Create New User* button allows us to create new utility
users to the system.

<img src="media/image17.png" width="396" height="287" />

**Image 16: Create Utility User**

User’s *Email* address, *Utility*, *Base Role*, *User Role* (Additional
roles), and *Password* can be set to create a new user. *Email*,
*Password* and *Confirm Password* are mandatory fields.

Modifying user information can be done using the *Edit* button. The
*Utility* field cannot be changed, however *Email*, *Base Role*, *User
Role*, and *Password* can be modified.

<img src="media/image18.png" width="452" height="283" />

**Image 17: Edit Utility User**

To delete a user, the *Delete* button is used, which displays a warning
message confirming if the user can be deleted.

<img src="media/image19.png" width="480" height="155" />

**Image 18: Delete Utility User**

<span id="_tyjcwt" class="anchor"><span id="_Toc490149008" class="anchor"></span></span>Account Users (URL: /account/users)
---------------------------------------------------------------------------------------------------------------------------

The Account users’ manage screen will contain *Utility*, *Id*, *Email*,
and *Account Id* of all the account aligned to a Utility. Only Utility
users and Admin (ESI) can access this screen, so that they can manage
account information.
<img src="media/image20.png" width="624" height="181" />

**Image 19: Account User Login**

They can add new users to the system by using the *Create New User*
button.

<img src="media/image21.png" width="457" height="266" />

**Image 20: Create Account User**

*Email/UserName*, *Account Id*, *Utility code*, and *Password* fields
are available. On saving the above information an account user can be
created. *Email/UserName*, *Account Id*, *Choose Password* and *Confirm
Password* fields are mandatory.

The *Edit* button allows editing the user information which involves
modifying *Email/UserName*, *Account Id* and *Password* fields. If an
Admin logs into the system *Utility code* field will be greyed out.
However, if a Utility user logs in the *Utility code* field will not be
displayed.

<img src="media/image22.png" width="422" height="268" />

**Image 21: Edit Account User**

To delete a user from the Utility, *Delete* button can be used. On
deleting a warning message is displayed as shown in the image:

<img src="media/image23.png" width="473" height="149" />

**Image 22: Delete Account User**

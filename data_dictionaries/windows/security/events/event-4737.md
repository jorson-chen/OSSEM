# Event ID 4737: A security-enabled global group was changed.

## Description

See event _[4735](event-4735.md): A security-enabled local group was changed._ Event 4737 is the same, but it is generated for a **global** security group instead of a **local** security group. All event fields, XML, and recommendations are the same. The type of group is the only difference.

  > [!IMPORTANT]
  > Event 4737(S) generates only for domain groups, so the Local sections in event [4735](event-4735.md) do not apply.

[MS Source](https://github.com/MicrosoftDocs/windows-itpro-docs/blob/b7c0643659189d384c8fa4b234256bdaef176b02/windows/security/threat-protection/auditing/audit-security-group-management.md#L62)

## Event Log Illustration & Event XML

[MS Source](https://github.com/MicrosoftDocs/windows-itpro-docs/blob/master/windows/security/threat-protection/auditing/event-4735.md)

## Data Dictionary

|	Standard Name	|	Field Name	|	Type	|	Description	|	Sample Value	|
|	----------------	|	----------------	|	----------------	|	----------------	|	----------------	|
|	group_name	|	TargetUserName	|	string	|	the name of the group that was changed. For example: ServiceDesk	|	AccountOperators\_NEW	|
|	group_domain	|	TargetDomainName	|	string	|	SID of changed group.	|	CONTOSO	|
|	group_sid	|	TargetSid	|	string	|	SID of changed group.	|	S-1-5-21-3457937927-2839227994-823803824-6605	|
|	user_sid	|	SubjectUserSid	|	string	|	SID of account that requested the “change group” operation. Event Viewer automatically tries to resolve SIDs and show the account name. If the SID cannot be resolved, you will see the source data in the event.	|	S-1-5-21-3457937927-2839227994-823803824-1104	|
|	user_name	|	SubjectUserName	|	string	|	the name of the account that requested the “change group” operation.	|	dadmin	|
|	user_domain	|	SubjectDomainName	|	string	|	subject’s domain or computer name.	|	CONTOSO	|
|	user_logon_id	|	SubjectLogonId	|	integer	|	hexadecimal value that can help you correlate this event with recent events that might contain the same Logon ID, for example, “4624: An account was successfully logged on.”	|	0x3031e	|
|	user_privilege_list	|	PrivilegeList	|	string	|	the list of user privileges which were used during the operation, for example, SeBackupPrivilege. This parameter might not be captured in the event, and in that case appears as “-”. See full list of user privileges in “Table 8. User Privileges.”.	|	-	|
|	group_sam_name	|	SamAccountName	|	string	|	This is a new name of changed group used to support clients and servers from previous versions of Windows (pre-Windows 2000 logon name). If the value of sAMAccountNameattribute of group object was changed, you will see the new value here. For example: ServiceDesk. For local groups it is simply a new name of the group, if it was changed.	|	AccountOperators\_NEW	|
| group_sid_history	|	SidHistory	|	string	|	contains previous SIDs used for the object if the object was moved from another domain. Whenever an object is moved from one domain to another, a new SID is created and becomes the objectSID. The previous SID is added to the sIDHistory property. If the value of sIDHistory attribute of group object was changed, you will see the new value here. For local groups it is not applicable and always has “-“ value.	|	-	|
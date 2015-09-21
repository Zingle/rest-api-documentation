# Resource Overview
Resource | Description
--- | ---
Account | An Account is the master record for a Business that uses Zingle.  As the developer you will be granted access to specific Accounts, and be provided the ability to perform operations on their behalf.  An Account is a container for one or more Services.
Service | A Service is a distinct messaging center that contains collections of conversations with Contacts. 
Plan | Every Service must have an associated Plan.  The plan defines the messaging limitations, features, and cost of the Zingle Service.
Contact | Contacts are customers to the Business. They are individuals that communicate in a two-way conversation with a Zingle Service.
Label | Labels are customizeable colored tags that can be applied to Contacts. Services may message all Contacts with a given Label for group messaging capabilities.
Custom Field | Custom Fields provide the ability to add variable meta data to Contacts. Custom Fields are useful for maintaining relevant stateful information about your Contacts.
Custom Field Option | Custom Fields may be either simple types (like a string), or be an option list.  Custom Field Options are the invididual values within an option list.
Custom Field Value | When updating Custom Field data on a Contact, you are actually updating a Custom Field Value object.  This entity maps a Custom Field to the value on the Contact.
Channel Type | Channel Types are the medium that facilitate communication between the Contact and the Service.  Example Channel Types are: Phone Number, Email Address, and User Defined.
Service Channel | A Service Channel is the way Contacts can communicate with a Service.  A Service Channel might have a Channel Type of Phone Number, with a Channel Value of +18585555555.  Service Channels **must** be unique across the entire Zingle platform.  A Service may contain multiple Service Channels of differing Channel Types.
Contact Channel | A Contact Channel is the way Services can communicate with a Contact.  A Contact Channel might have a Channel Type of Phone Number, with a Channel Value of +18585555555.  Contact Channels **must** be unique within a Zingle Service.  A Contact may contain multiple Contact Channels of differing Channel Types.
Message | Messages define the sender, recipient(s), message body, and attachments.  Messages are sent to/from Contacts, Services and Labels via Channels.
Message Correspondent | Message Correspondents are the abstract representation of either the Sender or Recipient on a Message.
Message Attachment | Message Attachments provide the ability to add binary data, such as images, to messages.
Automation | Automations perform triggered tasks, based on conditions, within the Zingle platform without any direct user interaction.  Tasks include messaging contacts, applying labels, applying custom fields, printing to Zingle Printers, and much more.

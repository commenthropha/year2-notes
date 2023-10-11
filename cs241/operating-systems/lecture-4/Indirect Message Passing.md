In indirect message passing:
- Messages are directed to and received from mailboxes:
	`send(mailboxID, msg)` and `receive(mailboxID, msg)`
- A link may be associated with many processes and vice versa
	- There is a many-to-many relationship between processes and mailboxes
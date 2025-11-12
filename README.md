Performance & Scaling Notes (talking points)

Use proper indexing for filters (status, user_id, due_at).

For high write volumes, consider append-only event log or partitioning by date.

Replace file-based tag ops with normalized lookups + caching in app layer.

Use connection pooling and prepared statements in application code.

Interview Script (30–45s)

“I designed a normalized Task Manager schema with users, tasks, tags, and an audit log. I enforced integrity with foreign keys and unique constraints, used partial indexes for common filters (overdue/due date), and added triggers to keep timestamps and an audit trail. I implemented a transactional stored function to create tasks with tags safely, and wrote reporting queries using CTEs and aggregates. This structure supports easy horizontal scaling and is testable—unit tests can exercise stored functions and queries using a test DB.”

### Backups vs Snapshots: Not the same thing (and why compliance teams care).
A lot of teams treat snapshots like backups. They’re not.
Here’s the difference in simple cloud terms:

🔹 Snapshots = Point-in-time captures
Fast, cheap, great for quick rollback, patch testing, or VM recovery but they usually live in the same failure domain (same region/account/storage system).

🔹 Backups = Long-term protection
Policy-driven, often geo-redundant, encrypted, immutable, and designed for disaster recovery + audits.

Now the compliance angle:
Frameworks like ISO 27001, SOC 2, HIPAA, etc. don’t just ask
“Do you have data recovery?”
 They ask:
 ✅ Is it tamper-proof?
 ✅ Is it retained properly?
 ✅ Can you restore independently of the source?
 ✅ Is it verifiable during audits?

Snapshots alone usually fail that test.
Backups are built to pass it.
In real-world cloud operations, mature environments use both:
Snapshots for operational recovery
Backups for resilience, ransomware protection, and compliance
If your DR strategy only says “we take snapshots”, you’re not covered, you’re just hoping.

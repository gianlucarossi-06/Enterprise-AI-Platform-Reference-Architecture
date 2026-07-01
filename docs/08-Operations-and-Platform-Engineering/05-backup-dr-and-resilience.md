# Backup, Disaster Recovery, and Resilience

The platform should separate runtime state, configuration state, and audit state so each can be protected with the correct recovery strategy.

Key practices:
- define RPO and RTO per service
- back up platform metadata and policies
- protect immutable audit data
- rehearse restore procedures
- validate cross-region or cross-fault-domain recovery

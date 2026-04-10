# Backend

This folder contains the backend services and infrastructure code used to run LiT on AWS.

## Main areas

- `lambdas/`: API Lambda handlers and Java shared modules
- `containers/`: containerized services (LiveKit, backend bot, translation pipeline integration)
- `terraform/`: infrastructure provisioning for cloud resources
- `localHost/`: local endpoint testing helpers
- `shared/`: common code used across backend components
# TODO — Online Student Verification & Clearance System

## Phase 1: Foundation
- [ ] Initialize Django project and apps
- [ ] Configure environment variables (DEBUG, SECRET_KEY, DB)
- [ ] Set up PostgreSQL database
- [ ] Enable HTTPS-ready settings
- [ ] Configure media/file storage (local → S3-ready)

## Phase 2: Authentication & Roles
- [ ] Implement custom User model with roles (student, officer, admin)
- [ ] Enforce role-based access control (RBAC)
- [ ] Create permissions layer for API endpoints
- [ ] Secure authentication (session or JWT)

## Phase 3: Student Management
- [ ] Create StudentProfile model
- [ ] Link StudentProfile to User (one-to-one)
- [ ] Validate unique matric numbers
- [ ] Student profile API (view/update)

## Phase 4: Units & Officers
- [ ] Create Unit model (Library, Bursary, etc.)
- [ ] Create Officer model linked to Unit
- [ ] Assign officers to units (admin-only)
- [ ] Restrict officers to their assigned units

## Phase 5: Clearance Workflow
- [ ] Create ClearanceRequest model
- [ ] Auto-generate ClearanceItems per active unit
- [ ] Implement per-unit status tracking (pending/approved/rejected)
- [ ] Compute overall clearance status server-side
- [ ] Prevent duplicate or invalid state transitions

## Phase 6: Document Handling
- [ ] Implement secure document upload
- [ ] Restrict file types and size
- [ ] Store files outside web root
- [ ] Link documents to ClearanceItems

## Phase 7: Officer Actions
- [ ] Officer dashboard (pending items)
- [ ] Approve clearance item with optional comment
- [ ] Reject clearance item with mandatory comment
- [ ] Enforce authorization per unit

## Phase 8: Audit & Logging
- [ ] Implement AuditLog model
- [ ] Log approvals, rejections, and certificate generation
- [ ] Store timestamped action metadata

## Phase 9: Certificate Generation
- [ ] Generate clearance certificate (PDF)
- [ ] Embed student and approval metadata
- [ ] Generate QR code for verification
- [ ] Persist certificate record with UUID
- [ ] Auto-generate certificate when all units approve

## Phase 10: Verification
- [ ] Public certificate verification endpoint
- [ ] Validate QR UUID
- [ ] Return read-only verification result
- [ ] Prevent enumeration attacks

## Phase 11: Notifications
- [ ] Email notification on approval/rejection
- [ ] Email notification on final clearance
- [ ] Graceful failure if email service is unavailable

## Phase 12: Admin Dashboard
- [ ] System overview (pending / cleared / rejected)
- [ ] Reports per unit and department
- [ ] User and unit management
- [ ] Clearance history search

## Phase 13: Testing
- [ ] Unit tests for models
- [ ] Integration tests for workflow
- [ ] Permission and authorization tests
- [ ] Certificate generation tests

## Phase 14: Deployment Readiness
- [ ] Gunicorn configuration
- [ ] Nginx reverse proxy
- [ ] Static and media handling
- [ ] Database backup strategy
- [ ] Security hardening checklist

## Phase 15: Documentation
- [ ] API documentation
- [ ] System architecture diagram
- [ ] ERD and workflow diagrams
- [ ] Deployment guide

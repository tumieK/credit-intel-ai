users
- id (UUID, PK)
- email (unique)
- hashed_password
- is_active
- created_at

roles
- id (UUID, PK)
- name (admin, analyst, client)

user_roles
- user_id (FK)
- role_id (FK)

applicants
- id (UUID, PK)
- user_id (FK)
- applicant_type (individual | sme)
- id_number (nullable)
- company_reg_number (nullable)
- created_at

applications
- id (UUID, PK)
- applicant_id (FK)
- status (draft, submitted, reviewed, approved, rejected)
- submitted_at

documents
- id (UUID, PK)
- application_id (FK)
- document_type (bank_statement, payslip, invoice, affidavit)
- storage_path
- uploaded_at

document_analysis
- id (UUID, PK)
- document_id (FK)
- summary
- extracted_data (JSONB)
- risk_flags (JSONB)
- created_at

risk_scores
- id (UUID, PK)
- application_id (FK)
- overall_score (numeric)
- explanation
- generated_by (AI | analyst)
- created_at

risk_factors
- id (UUID, PK)
- risk_score_id (FK)
- factor_name
- impact_score

subscriptions
- id (UUID, PK)
- user_id (FK)
- plan
- status
- started_at
- ended_at

payments
- id (UUID, PK)
- user_id (FK)
- amount
- provider
- status
- created_at

audit_logs
- id (UUID, PK)
- user_id (FK)
- action
- entity
- entity_id
- timestamp

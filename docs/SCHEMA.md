# Loan Origination — Schema

Tables this module reads from / writes to. Columns are extracted from the SQL migrations.

## `loans`

| Column | Type |
|---|---|
| `id` | UUID |
| `loan_number` | VARCHAR(50) |
| `borrower_id` | UUID |
| `loan_officer_id` | UUID |
| `product_id` | UUID |
| `program_id` | UUID |
| `status` | VARCHAR(50) |
| `loan_amount` | DECIMAL(15,2) |
| `appraised_value` | DECIMAL(15,2) |
| `ltv` | DECIMAL(5,2) |
| `credit_score` | INT |
| `dti` | DECIMAL(5,2) |
| `purpose` | VARCHAR(50) |
| `occupancy_type` | VARCHAR(50) |
| `property_address` | VARCHAR(255) |
| `property_city` | VARCHAR(100) |
| `property_state` | VARCHAR(50) |
| `property_postal_code` | VARCHAR(20) |
| `lock_date` | DATE |
| `lock_expiration_date` | DATE |
| `created_at` | TIMESTAMPTZ |
| `updated_at` | TIMESTAMPTZ |
| `created_by` | UUID |
| `data_source` | VARCHAR(50) |
| `external_id` | VARCHAR(255) |
| `api_payload` | JSONB |

## `loan_timeline_events`

| Column | Type |
|---|---|
| `id` | UUID |
| `loan_id` | UUID |
| `event_type` | VARCHAR(50) |
| `event_source` | VARCHAR(50) |
| `title` | VARCHAR(255) |
| `description` | TEXT |
| `occurred_at` | TIMESTAMPTZ |
| `metadata` | JSONB |
| `created_by` | UUID |
| `created_at` | TIMESTAMPTZ |

## `loan_milestones`

| Column | Type |
|---|---|
| `id` | UUID |
| `loan_id` | UUID |
| `milestone_type` | VARCHAR(50) |
| `name` | VARCHAR(150) |
| `due_date` | DATE |
| `completed_at` | TIMESTAMPTZ |
| `notes` | TEXT |
| `external_id` | VARCHAR(255) |
| `created_by` | UUID |
| `created_at` | TIMESTAMPTZ |
| `updated_at` | TIMESTAMPTZ |

## `loan_conditions`

| Column | Type |
|---|---|
| `id` | UUID |
| `loan_id` | UUID |
| `condition_type` | VARCHAR(20) |
| `category` | VARCHAR(100) |
| `description` | TEXT |
| `status` | VARCHAR(30) |
| `due_date` | DATE |
| `received_at` | TIMESTAMPTZ |
| `notes` | TEXT |
| `external_id` | VARCHAR(255) |
| `created_by` | UUID |
| `created_at` | TIMESTAMPTZ |
| `updated_at` | TIMESTAMPTZ |

> Row Level Security is enabled on all tables. Never disable it.


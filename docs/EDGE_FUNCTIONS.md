# Loan Origination — Edge Functions

Server-side functions used by this module (descriptions read from each function's source).

## `transition-loan-status`

Transition Loan Status — validates stage transition, updates status, auto-creates milestones, and records timeline events.

Source: `supabase/functions/transition-loan-status/index.ts`

## `import-loans-csv`

Validated CSV import for loans (dry-run or commit). Upsert by data_source + external_id. Requires admin app role or loans:import permission. Uses service role after authorization.

Source: `supabase/functions/import-loans-csv/index.ts`

## Shared utilities

- `supabase/functions/_shared/dispatch-notification.ts`


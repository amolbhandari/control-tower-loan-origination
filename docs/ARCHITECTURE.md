# Loan Origination — Architecture

End-to-end loan file lifecycle: pipeline, detail, application intake, status transitions, milestones, and timeline.

This module is organised into the layers below. Every path listed is a real file in the repository.

## Data layer (Supabase)

- `loans`
- `loan_timeline_events`
- `loan_milestones`
- `loan_conditions`

All tables enforce Row Level Security; reads/writes are scoped to the caller.

## Service layer (React Query hooks)

- `src/hooks/useLoans.ts` — `useLoans`
- `src/hooks/useLoanApplication.ts` — `useLoanApplication`
- `src/hooks/useLoanTransitions.ts` — `useLoanTransitions`
- `src/hooks/useLoanTimeline.ts` — `useLoanTimeline`
- `src/hooks/useLoanMilestones.ts` — `useLoanMilestones`

## Presentation layer

- Page: `src/pages/Loans.tsx`
- Page: `src/pages/LoanDetail.tsx`
- Page: `src/pages/LoanForm.tsx`
- Page: `src/pages/LoanImport.tsx`
- Component: `src/components/loans/LoanTimeline.tsx`
- Component: `src/components/loans/MilestoneTracker.tsx`
- Component: `src/components/loans/RiskBadge.tsx`
- Component: `src/components/loans/LoanDisclosuresCard.tsx`

## Backend layer (Supabase Edge Functions)

- `supabase/functions/transition-loan-status`
- `supabase/functions/import-loans-csv`
- Shared util: `supabase/functions/_shared/dispatch-notification.ts`

## Entry point

`src/pages/Loans.tsx`


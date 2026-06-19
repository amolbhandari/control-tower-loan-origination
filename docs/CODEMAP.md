# Loan Origination — Code Map

Every file shipped with this module.

## Pages

```
src/pages/Loans.tsx
src/pages/LoanDetail.tsx
src/pages/LoanForm.tsx
src/pages/LoanImport.tsx
```

## Hooks

```
src/hooks/useLoans.ts
src/hooks/useLoanApplication.ts
src/hooks/useLoanTransitions.ts
src/hooks/useLoanTimeline.ts
src/hooks/useLoanMilestones.ts
```

## Components

```
src/components/loans/LoanTimeline.tsx
src/components/loans/MilestoneTracker.tsx
src/components/loans/RiskBadge.tsx
src/components/loans/LoanDisclosuresCard.tsx
```

## Edge functions

```
supabase/functions/transition-loan-status/index.ts
supabase/functions/import-loans-csv/index.ts
```

## Shared edge utilities

```
supabase/functions/_shared/dispatch-notification.ts
```


# Loan Origination — Integration

How to drop the **Loan Origination** module into a React + Vite + Supabase app.

## 1. Dependencies

```bash
npm i @supabase/supabase-js @tanstack/react-query react-router-dom lucide-react sonner
```

## 2. Environment

```bash
VITE_SUPABASE_URL=...
VITE_SUPABASE_ANON_KEY=...
```

## 3. Database

Apply migrations that create these tables (RLS enabled):

- `loans`
- `loan_timeline_events`
- `loan_milestones`
- `loan_conditions`

## 4. Edge functions

Deploy the following functions:

```bash
npx supabase functions deploy transition-loan-status
npx supabase functions deploy import-loans-csv
```

They depend on these shared utilities (copy alongside the functions):

- `supabase/functions/_shared/dispatch-notification.ts`

## 5. Routing

Register the module's pages, e.g.:

```tsx
// <Route path="..." element={<Loans />} />
// <Route path="..." element={<LoanDetail />} />
// <Route path="..." element={<LoanForm />} />
// <Route path="..." element={<LoanImport />} />
```

Entry point: `src/pages/Loans.tsx`.


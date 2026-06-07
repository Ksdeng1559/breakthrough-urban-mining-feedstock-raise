# Supabase Schema

## Purpose

This schema supports the RIOS/OpenClaw feedstock acquisition workflow for Breakthrough Urban Mining / MineTeck.

---

## organizations

```sql
create table organizations (
  id uuid primary key default gen_random_uuid(),
  name text not null,
  industry text,
  location text,
  website text,
  employee_count integer,
  facility_count integer,
  signal_score numeric,
  feedstock_probability_score numeric,
  relationship_status text,
  notes text,
  created_at timestamptz default now()
);
```

---

## contacts

```sql
create table contacts (
  id uuid primary key default gen_random_uuid(),
  organization_id uuid references organizations(id),
  name text,
  title text,
  email text,
  phone text,
  linkedin_url text,
  role_type text,
  confidence_score numeric,
  relationship_status text,
  last_contacted_at timestamptz,
  created_at timestamptz default now()
);
```

---

## feedstock_opportunities

```sql
create table feedstock_opportunities (
  id uuid primary key default gen_random_uuid(),
  organization_id uuid references organizations(id),
  signal_type text,
  signal_source text,
  feedstock_type text,
  estimated_weight_tonnes numeric,
  estimated_grade text,
  estimated_purchase_price_per_tonne numeric,
  estimated_transport_cost numeric,
  estimated_processing_cost numeric,
  estimated_recovery_value numeric,
  estimated_gross_margin numeric,
  confidence_score numeric,
  stage text,
  assigned_to text,
  created_at timestamptz default now()
);
```

---

## feedstock_yield_assumptions

```sql
create table feedstock_yield_assumptions (
  id uuid primary key default gen_random_uuid(),
  feedstock_type text,
  gold_grams_per_tonne_low numeric,
  gold_grams_per_tonne_base numeric,
  gold_grams_per_tonne_high numeric,
  silver_grams_per_tonne_low numeric,
  silver_grams_per_tonne_base numeric,
  silver_grams_per_tonne_high numeric,
  copper_kg_per_tonne_low numeric,
  copper_kg_per_tonne_base numeric,
  copper_kg_per_tonne_high numeric,
  source text,
  approved_by text,
  created_at timestamptz default now()
);
```

---

## actual_lot_results

```sql
create table actual_lot_results (
  id uuid primary key default gen_random_uuid(),
  opportunity_id uuid references feedstock_opportunities(id),
  feedstock_type text,
  actual_weight_tonnes numeric,
  actual_purchase_cost numeric,
  actual_transport_cost numeric,
  actual_processing_cost numeric,
  actual_gold_recovered numeric,
  actual_silver_recovered numeric,
  actual_copper_recovered numeric,
  actual_revenue numeric,
  actual_margin numeric,
  lessons_learned text,
  created_at timestamptz default now()
);
```

---

## Notes

The `actual_lot_results` table is strategically important because it turns real acquisition and recovery outcomes into proprietary MineTeck intelligence.

# Nav Bar Update

The current nav is: **Templates | Documentation | Tutorials | Blog | About | Join Us**

Two options:

## Option A: Dropdown (Recommended)

Rename "Templates" to "Get Started" or "Projects" and make it a dropdown:

```
Get Started ▾
  ├── Templates
  └── Built Ons
```

Or keep "Templates" as the label with a dropdown:

```
Templates ▾
  ├── Templates
  └── Built Ons
```

The dropdown already has a pattern in the nav — "Join Us" is a dropdown. So this would be consistent.

**Implementation:** The "Templates" link currently goes to `/templates.html`. Change it to a dropdown where "Templates" links to `/templates.html` (which now also includes the Built Ons section) and "Built Ons" links to an anchor on that page (`/templates.html#built-ons`) or to a separate `/built-ons/` index if you want one.

## Option B: Separate Nav Item

Add "Built Ons" as its own nav item after "Templates":

```
Templates | Built Ons | Documentation | Tutorials | Blog | About | Join Us
```

Simpler but adds width to the nav. Probably fine since "Built Ons" is short.

**Links to:** `/templates.html#built-ons` (anchor on templates page) or `/built-ons/` (if you create a Built Ons index page).

## Recommendation

Go with Option A (dropdown) for now. It groups related things together and doesn't add width. You can always split it out later if Built Ons grows into its own thing.

If you do want a standalone `/built-ons/` index page later (listing all Built Ons with descriptions), that's easy to add — but for now the templates page with the Built Ons section added is enough.

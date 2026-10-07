# Frontend

Planned stack: Next.js, React, TypeScript, Tailwind CSS, MapLibre GL JS, TanStack Query, React Hook Form and Zod. shadcn/ui is optional where useful; Vitest/React Testing Library/Playwright support relevant tests. Add packages when their feature is implemented and verify current version compatibility.

Feature organization under apps/web includes globe, country, auth, my-world, visits and trips as implemented. Keep globe components, layers, hooks, utilities and types focused rather than accumulating every product rule in one Globe.tsx.

## State and interaction

Server state uses TanStack Query; URL state uses Next.js search parameters; local state uses React; forms use React Hook Form and Zod when needed. Do not add Redux or Zustand by default.

Conceptual layers: EXPLORE, VISITED, BUCKET_LIST, COST, WEATHER, TRAVEL_ADVICE, NEWS and UNESCO. Implement Explore for M1, other layers incrementally. URL-address important state, for example `/world?layer=visited` and `/world?layer=travel-advice&country=IR`. Browser navigation and deep links must restore selection; invalid/unsupported values need deterministic fallback.

The globe is primarily client-side. Public country content can use Next.js rendering. Map clicks resolve a stable supported identifier, then fetch the internal country API. The frontend never directly calls external intelligence providers or embeds editorial research in components.

Provide accessible keyboard/search/list country selection alongside pointer globe interactions, understandable loading/empty/error states, responsive panels and suitable focus handling. Generated OpenAPI types must stay in sync with actual endpoints.

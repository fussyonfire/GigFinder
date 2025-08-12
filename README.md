# Gig Finder for Emerging DJs

A lightweight web app that helps small venue owners discover and book local DJs, and lets DJs showcase mixes and manage availability.

## Why
- Venues struggle to find reliable local DJs with the right vibe/genre.
- Emerging DJs need a simple way to show mixes and availability.
- Reduce back-and-forth messaging and booking mistakes.

## Users
- **Venue Owners/Managers** (primary): search, preview mixes, check availability, request bookings.
- **DJs** (primary): set up profile, upload mixes, manage calendar, respond to bookings.
- **Promoters/Staff** (secondary): browse talent, assist with bookings.

## Project Goals
- Fast, mobile-first flow for searching and booking.
- Clear, consistent profile layout with embedded audio.
- Error-resistant booking process with confirmations.
- Accessibility built-in (WCAG quick wins).

## Non-Goals (for MVP)
- Payments/escrow.
- Contract generation.
- Complex messaging threads (basic contact is enough).

## Human Factors (Nielsen Heuristics) – Commitments
- **Visibility of system status**: loading/play states, booking progress indicators.
- **Match to real world**: “gig”, “set time”, “load-in”, calendar metaphors.
- **User control & freedom**: cancel/new search, undo booking request.
- **Consistency/standards**: same profile layout for every DJ; standard media controls.
- **Error prevention**: validate booking forms; disable past dates.
- **Recognition not recall**: genre chips, icons with labels.
- **Flexibility/efficiency**: filters, keyboard shortcuts later.
- **Aesthetic & minimalist**: uncluttered results grid; focus on audio + availability.
- **Error recovery**: friendly error messages with next steps.
- **Help & docs**: “Getting started” for DJs & venues.

## Accessibility (WCAG quick wins)
- Sufficient colour contrast; dark mode accessible.
- Keyboard navigation for all controls (incl. audio player).
- Alt text for images; captions/transcripts for promo videos.
- Don’t use colour alone to convey state; add icons/text.
- Focus states and skip-to-content link.

## Pages (MVP)
- **Home/Search**: search bar + filters (genre, city, date).
- **Results Grid**: cards with name, genre chips, quick play button.
- **DJ Profile**: bio, embedded audio player, photos, availability calendar, “Request booking”.
- **Booking Flow**: date/time selector → form → confirmation.
- **DJ Dashboard**: profile editor, upload mixes, manage availability, upcoming gigs.

## Data Model (draft)
- DJ: id, name, bio, genres[], socials, media[], availability[]
- Venue: id, name, location, capacity, contact
- Booking: id, djId, venueId, date, time, status{requested|accepted|declined|cancelled}
- Media: id, djId, url, type{mix|video}, duration

## Milestones
- Week 3: Research + ideation + wireframes committed.
- Week 4: Criteria defined + 2–3 design options.
- Week 5: Decision matrix + selected design + low/hi-fi prototype start.
- Week 10: Interactive prototype ready.
- Week 13: Evaluation report.

## Repo Structure
```
/docs          # brief, criteria, decision matrix
/ux            # wireframes, user journeys, notebook
/data          # sample csvs, content stubs
```

## How to Use this Repo Right Now
- Add sketches (photos or exports) to `/ux/wireframes` (create folder).
- Fill out `/docs/design_criteria.md` and `/docs/decision_matrix.csv`.
- Open the Jupyter notebook in `/ux/01_research_and_ideation.ipynb` and add notes.
- Commit early and often with meaningful messages.
